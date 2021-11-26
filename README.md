> #### ☑️ Has meta viewport
> Meta viewports optimize your app for mobile screens.
>
> 📖 [Web.dev - Document has a viewport meta tag](https://web.dev/viewport/?utm_source=lighthouse&utm_medium=devtools)

```html
<meta name="viewport" content="width=device-width, initial-scale=1" />
```
----------

> #### ☑️ Has open graph tags
> The Open Graph protocol enables any web page to become a rich object in a social graph. To turn a web page into a rich object, you need to add additional `meta` tags to your head.  
> The four required properties are:
> - `og:title` - The title of the object, usually will match the content of your `title` tag
> - `og:type` - The type of object, eg.: `article`, `profile`, `website`. *(To see all available object types visit the [object types section](https://ogp.me/#types) on the official page of open graph.)*
> - `og:image` - The URL of the image which will represent the object
> - `og:url` - The URL of your site where the object will take the user after interaction
>
> To see all other available open graph tags, visit the [official website](https://ogp.me/) of the open graph protocol.
>
> 📖 [The Open Graph protocol](https://ogp.me/)  
> 🛠️ [Facebook - Open Graph Object Debugger](https://developers.facebook.com/tools/debug/og/object)

```html
<!-- Example markup for the movie "The Rock" on IMDB -->
<meta property="og:title" content="The Rock" />
<meta property="og:type" content="video.movie" />
<meta property="og:url" content="http://www.imdb.com/title/tt0117500/" />
<meta property="og:image" content="http://ia.media-imdb.com/images/rock.jpg" />
```
----------

### Document head
ℹ️ *Apart from meta tags, there are a number of other tags in the head of the document that you should take care of.*

> #### ☑️ Doctype is set to HTML5
> The `<!DOCTYPE>` declaration must be the very first thing in your HTML document. It tells browsers what version of HTML the page is written in. You should always use the latest version which is HTML5.
>
> 📖 [W3Schools - HTML <!DOCTYPE> Declaration](https://www.w3schools.com/tags/tag_doctype.asp)  
> 🛠️ [SEO Site Checkup - Doctype Test](https://seositecheckup.com/tools/doctype-test)

```html
<!DOCTYPE html>
```
----------

> #### ☑️ Document has a title tag
> The title gives screen reader users an overview of the page, and search engine users rely on it heavily to determine if a page is relevant to their search.
> Titles shouldn't be too long or too short, try to keep the character count around 50-60.
>
> 📖 [Web.dev - Document has a title tag](https://web.dev/document-title/?utm_source=lighthouse&utm_medium=devtools)

```html
<!doctype html>
<html lang="en">
    <head>
        …
        <title>SEO Checklist</title>
        …
    </head>
    <body>
        …
    </body>
</html>
```
----------

> #### ☑️ Document has a valid hreflang
> hreflang links tell search engines what version of a page they should list in search results for a given language or region.
>
> 📖 [Web.dev - Valid href for document](https://web.dev/hreflang/?utm_source=lighthouse&utm_medium=devtools)

```html
<link rel="alternate" hreflang="en" href="https://my-site.com" />
<link rel="alternate" hreflang="es" href="https://es.my-site.com" />
<link rel="alternate" hreflang="de" href="https://de.my-site.com" />
```
----------

> #### ☑️ Favicon exists
> If your site has a favion, it can be included in the search results page.
>
> 📖 [Google Search Console - Define favicon to show in search results](https://support.google.com/webmasters/answer/9290858?hl=en)

```html
<link rel="shortcut icon" href="/path/to/favicon.ico" />
```
----------

### Document structure
ℹ️ *Document structure outlines how your html should be built up and shows what are the key factors that can affect your SEO.*

> #### ☑️ SEO friendly URLs
> SEO friendly URLs should only contain letters and number, dashes (-) or underscores (_). Try to avoid using spaces, signs or other special characters. Make them short and relevant to the topic. Try to incorporate keywords into them.
>
> 📖 [Google Search Console - Keep a simple URL structure](https://support.google.com/webmasters/answer/76329)  
> 📖 [Moz - URLs](https://moz.com/learn/seo/url)  
> 🛠️ [SEO Site Checkup - SEO Friendly URL Test](https://seositecheckup.com/tools/seo-friendly-url-test)

```html
<!-- 🔴 Don't -->
<a href="https://example.com/index.php?page=articles&order=desc">Latest articles</a>

<!-- ✅ Do -->
<a href="http://example.com/articles/latest">Latest articles</a>
```
----------

> #### ☑️ One H1 per page
> H1 should only be used as your main title. Headings help Google understand your text and the context of the page.
>
> 📖 [Webtips.dev - 10 Best Practices for HTML](https://www.webtips.dev/10-best-practices-for-html)  
> 📖 [Yoast - More than one H1](https://yoast.com/academy/seo-copywriting-training/single-h1/)
----------

> #### ☑️ Image elements have [alt] attributes
> Informative elements should aim for short, descriptive alternate text. Decorative elements can be ignored with an empty alt attribute.
>
> 📖 [Web.dev - Image elements have [alt] attributes](https://web.dev/image-alt/?utm_source=lighthouse&utm_medium=devtools)

```html
<!-- Images should have a short, descriptive alt text -->
<img src="..." alt="Diagram showing the steps of critical rendering path" />

<!-- If the image doesn't provide any value, still give it an empty alt tag -->
<img src="..." alt="" />
```
----------

> #### ☑️ Document uses legible font sizes
> Font sizes less than 12px are too small to be legible and require mobile visitors to “pinch to zoom” in order to read.
>
> 📖 [Web.dev - Document uses legible font sizes](https://web.dev/font-size/?utm_source=lighthouse&utm_medium=devtools)
----------

> #### ☑️ Tap targets are sized appropriately
> Interactive elements like buttons and links should be large enough (48x48px), and have enough space around them, to be easy enough to tap without overlapping onto other elements.
>
> 📖 [Web.dev - Tap targets are sized appropriately](https://web.dev/tap-targets/?utm_source=lighthouse&utm_medium=devtools)
----------

> #### ☑️ Document avoids plugins
> Search engines can't index plugin content, and many devices restrict plugins or don't support them.
> 
> Elements such as `embed`, `object` or `applet` are checked and if their MIME type matches any of the following:
> - `application/x-java-applet`
> - `application/x-java-bean`
> - `application/x-shockwave-flash`
> - `application/x-silverlight`
> - `application/x-silverlight-2`
> 
> Then it will be flagged as a plugin.
>
> 📖 [Web.dev - Document avoids plugins](https://web.dev/plugins/?utm_source=lighthouse&utm_medium=devtools)
----------

### Readability

> #### ☑️ Title width
> The document title not only shows up in the tab but is also shown in the Google search results page as a blue link. This is what users first see about your website on the search result page. To grab user attention, be short and to the point. Titles wider than 600px will be cut off so make sure your title is not too long. Also try to incorporate your main keyword.
>
> 📖 [Yoast - The ideal width of title](https://yoast.com/academy/all-around-seo-training/seo-title-width)
----------

> #### ☑️ Subheading distribution
> Most texts of over 300 words need subheadings to help the reader scan the text more easily. Using subheadings will not only make your text more readable and accessible, but will also help Google figure out what your content is about.  
> If you can, also incorporate your main keyphrase in the subheading.
>
> 📖 [Yoast - How to improve subheading distribution](https://yoast.com/academy/seo-copywriting-training/subheading-distribution/)
----------

> #### ☑️ Links have descriptive text
> Descriptive link text helps search engines understand your content.
>
> 📖 [Web.dev - Links have descriptive text](https://web.dev/link-text/?utm_source=lighthouse&utm_medium=devtools)

```html
<!-- 🔴 Don't -->
<p>To see more articles like this, <a href="articles.html">click here</a>.</p>

<!-- ✅ Do -->
<p>Are you interesed in more? Check out these <a href="articles.html">similar articles</a>.</p>
```
----------

> #### ☑️ Internal links
> Use internal links throughout your site. It helps Google get an idea about the structure and hierarchy of your page. You should have the most internal links pointing to a cornerstone content. This ways, the most important content on your site recieves the highest link value.  
> By adding internal links, you enable Google to understand:
> - The relevance of pages
> - The relationship between the pages
> - The value of each page
>
> Last but not least, it can help both users and search engines to nagivate your site more easily.
>
> 📖 [Yoast - Internal linking for SEO: Why and how?](https://yoast.com/internal-linking-for-seo-why-and-how/)
----------

> #### ☑️ Outbound links
> Outbound or external links are links that are pointing to other websites from your page. Using external links and linking to other relevant pages on the web can help search engines better understand the context of your site.
>
> 📖 [Moz - External Links](https://moz.com/learn/seo/external-link)
----------

> #### ☑️ Use of keyphrases
> The focus keyphrase – or keyword – is the search term that you want your page to rank for most. For blog posts, you should usually aim for long-tail keywords (keywords containing multiple words) as competition is lower for these. To help you decide on keywords, you can use tools such as [Google Trends](https://trends.google.com/trends), [Google Keyword Planner](https://ads.google.com/intl/en_gb/home/tools/keyword-planner/), [Answer The Public](https://answerthepublic.com/) or simply search for your proposed term on Google and let autosuggest show you what other people are searching for.
>
> Make sure that your keyphrase:
> - Appear in the title tag
> - Appears in subheadings
> - Appears in first paragraph
> - is unique, not used it before throughout your site
> - is used in the slug *(your SEO friendly URL)*
> - is used in meta description
> - is used in image [alt] attributes
> - is not too long
> - Density is between 1-3% *(number of times your keyphrase appears in a copy, eg.: your text is 100 words and 5 of those are your keywords than you have a keyword density of 5%)*
----------

> #### ☑️ Use of passive voice
> In most cases, active sentences are easier to understand than passive sentences. After writing your text, scan it for passive voice constructions. Always ask yourself: is a better, active alternative available? If there is, use it. If not, use the passive voice.
>
> 📖 [Yoast - Using and avoiding the passive voice](https://yoast.com/academy/seo-copywriting-training/passive-voice/)
----------

> #### ☑️ Use of transition words
> Transition words like **and**, **but**, **so**, **because** make it easier to read and understand a text. Although transition words don’t influence your SEO directly, they are one of the key factors to readability.
>
> 📖 [Yoast - Transition words: why and how to use them](https://yoast.com/academy/seo-copywriting-training/transition-words/)
----------

> #### ☑️ Text length
> You have a higher chance of ranking in Google if you have plenty of content on your page, preferably posts with 1000 words or more.  
> The reason this will help you rank higher:
> - Google will have more clue to determine what your page is about
> - The longer the text, the more often your keywords will appear in it
> - The more content there is, the more value it can give to users, making your site more relevant
>
> 📖 [Yoast - Text length: how long should a blog post be?](https://yoast.com/academy/seo-copywriting-training/text-length/)
----------

> #### ☑️ Length of paragraphs
> Paragraphs help break down your text into bite-size and easy-to-understand chunks. Big walls of text are hardly readable and tend to scare off visitors. Try to limit the length of your paragraphs to **200 words.**
>
> 📖 [Yoast - Writing shorter paragraphs: why and how](https://yoast.com/academy/seo-copywriting-training/paragraph-length/)
----------

> #### ☑️ Length of sentences
> Longer sentences are generally more difficult to read than shorter sentences. Dividing longer sentences into shorter ones can help improve readability.
>
> 📖 [Yoast - Writing shorter sentences](https://yoast.com/academy/seo-copywriting-training/sentence-length/)
----------

## 📊 Off-Site SEO
----------
ℹ️ *Off-Site SEO is not about technical details, but about marketing and promotion techniques.*

### Link building
ℹ️ *Link building is the process of getting other websites link back to your site. Backlinks are an important factor for search engines to determine which site to rank higher for which keyword.*

> #### ☑️ Amount of links
> Amount of links should not be excessive. Having too many links on a single page can hurt your SEO ranking as it is usually a sign of spam. The limit can depend on the type of site you have, whether you report news or provide services as a freelancer on a single landing page.
>
> 📖 [Varvy - How many links?](https://varvy.com/howmanylinks.html)  
> 📖 [Backlinko - Link Building](https://backlinko.com/link-building)
----------

> #### ☑️ Good vs bad links
> When dealing with links, quality is more important than quantity. The type of links you use on your website and you receive traffic from, can make or break your ranking.  
> We can divide good and bad links into two sub-categories: incoming and outgoing links. Some examples for both are listed below.
>
> Links that can be considered **good links:**
> - Links from high authority websites
> - Editorial links
> - Guest posting
> - Niche specific directories
>
> Links that can be considered **bad links:**
> - Links pointing to user profile pages
> - Links pointing to comments
> - Links pointing to dead websites
> - Links created with link builders
> - Links from foreign sites
> - Links from unrelated content
> - Links from paid links
> - Links from spammy comments
>
> 📖 [Moz - Types of Links](https://moz.com/beginners-guide-to-link-building/types-of-links)  
> 📖 [Ahrefs - Bad links](https://ahrefs.com/blog/bad-links/)
----------

> #### ☑️ The use of rel
> The `rel` attribute on a link tag specifies the relationship between the page and the linked URL. Used by Google to specify whether search spiders should follow the link. Only use if an `href` attribute is present linking to an external resource.
>
> The attribute it can take that is relevant to SEO:
> - **nofollow:** Indicates that the linked document is not endorsed by the author of this one. Do not confuse with **noopener** or **noreferrer**.
>
> 📖 [MDN web docs - Link types](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types)  
> 📖 [W3Schools - rel attribute](https://www.w3schools.com/TAGS/att_a_rel.asp)
----------

## 📚 Other Resources
- 📖 [Google Search Console - SEO Starter Guide](https://support.google.com/webmasters/answer/7451184?hl=en&ref_topic=9460495)
- 📖 [Google Search Console - Webmaster Guidelines](https://support.google.com/webmasters/answer/35769)
- 📖 [Moz - SEO Learning Center](https://moz.com/learn/seo)
- 📖 [Moz - The Beginners Guide to SEO](http://d2eeipcrcdle6.cloudfront.net/guides/Moz-The-Beginners-Guide-To-SEO.pdf)
- 📖 [TutorialsPoint - SEO Tutorials](http://www.tutorialspoint.com/seo/index.htm)
- 📖 [Ahrefs - The Noob Friendly Guide To Link Building](https://ahrefs.com/blog/link-building/)
- 📺 [Ahrefs - SEO For Beginners](https://www.youtube.com/watch?v=DvwS7cV9GmQ)
- 📺 [Ahrefs - SEO Checklist 2019](https://www.youtube.com/watch?v=taU9P98zfjk)
- 📺 [Backlinko - SEO Checklist 2020](https://www.youtube.com/watch?v=SEQBi9LtZjQ)
- 📺 [WordPress - Yoast SEO Tutorial 2019](https://www.youtube.com/watch?v=uNL82kDhG3w)
