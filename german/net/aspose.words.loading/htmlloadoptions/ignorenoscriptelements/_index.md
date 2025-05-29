---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft HtmlLoadOptions IgnoreNoscriptElements Ihr HTML-Parsing durch die Steuerung von Noscript-Elementen verbessert. Verbessern Sie noch heute Ihre Web-Performance!
type: docs
weight: 40
url: /de/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob &lt;noscript&gt; HTML-Elemente ignoriert werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Bemerkungen

Wie MS Word unterstützt Aspose.Words keine Skripte und lädt standardmäßig Inhalte von &lt;noscript&gt;-Elementen in das resultierende Dokument. In den meisten Browsern werden jedoch Skripte unterstützt, und Inhalte von &lt;noscript&gt; sind nicht sichtbar. Setzen Sie diese Eigenschaft auf`WAHR` zwingt Aspose.Words, alle &lt;noscript&gt;-Elemente zu ignorieren und hilft dabei, Dokumente zu erstellen, die dem, was in Browsern angezeigt wird, ähnlicher sind.

## Beispiele

Zeigt, wie &lt;noscript&gt;-HTML-Elemente ignoriert werden.

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

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
