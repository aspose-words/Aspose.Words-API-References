---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IgnoreNoscriptElements di HtmlLoadOptions migliora l'analisi HTML controllando gli elementi noscript. Migliora le prestazioni del tuo sito web oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

Ottiene o imposta un valore che indica se ignorare gli elementi HTML &lt;noscript&gt;. Il valore predefinito è `falso` .

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## Osservazioni

Come MS Word, Aspose.Words non supporta gli script e, per impostazione predefinita, carica il contenuto degli elementi &lt;noscript&gt; nel documento risultante. Nella maggior parte dei browser, tuttavia, gli script sono supportati e il contenuto di &lt;noscript&gt; non è visibile. Impostando questa proprietà su`VERO` forza Aspose.Words a ignorare tutti gli elementi &lt;noscript&gt; e aiuta a produrre documenti che sembrano più simili a ciò che viene visualizzato nei browser.

## Esempi

Mostra come ignorare gli elementi HTML &lt;noscript&gt;.

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

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
