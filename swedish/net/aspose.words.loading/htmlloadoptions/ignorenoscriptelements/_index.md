---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlLoadOptions IgnoreNoscriptElements förbättrar din HTML-parsning genom att kontrollera noscript-element. Förbättra din webbprestanda idag!
type: docs
weight: 40
url: /sv/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Hämtar eller anger ett värde som anger om &lt;noscript&gt; HTML-element ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Anmärkningar

Precis som i MS Word stöder inte Aspose.Words skript och laddar som standard innehållet från &lt;noscript&gt; elements till det resulterande dokumentet. I de flesta webbläsare stöds dock skript och innehållet från &lt;noscript&gt; syns inte. Om du ställer in den här egenskapen på`sann` tvingar Aspose.Words att ignorera alla &lt;noscript&gt;-element och hjälper till att producera dokument som ser närmare ut som vad som visas i webbläsare.

## Exempel

Visar hur man ignorerar &lt;noscript&gt; HTML-element.

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

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
