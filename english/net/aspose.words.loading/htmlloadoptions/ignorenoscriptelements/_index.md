---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words for .NET
description: Discover how the HtmlLoadOptions IgnoreNoscriptElements property enhances your HTML parsing by controlling noscript elements. Improve your web performance today!
type: docs
weight: 40
url: /net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Gets or sets a value indicating whether to ignore &lt;noscript&gt; HTML elements. Default value is `false`.

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Remarks

Like MS Word, Aspose.Words does not support scripts and by default loads content of &lt;noscript&gt; elements into the resulting document. In most browsers, however, scripts are supported and content from &lt;noscript&gt; is not visible. Setting this property to `true` forces Aspose.Words to ignore all &lt;noscript&gt; elements and helps to produce documents that look closer to what is seen in browsers.

## Examples

Shows how to ignore &lt;noscript&gt; HTML elements.

```csharp
const string html = @"
    <html>
      <head>
        <title>NOSCRIPT</title>
          <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">
          <script type=""text/javascript"">
            alert(""Hello, world!"");
          </script>
      </head>
    <body>
      <noscript><p>Your browser does not support JavaScript!</p></noscript>
    </body>
    </html>";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.IgnoreNoscriptElements = ignoreNoscriptElements;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

### See Also

* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
