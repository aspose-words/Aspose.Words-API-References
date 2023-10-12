---
title: HtmlFixedSaveOptions.PageMargins
second_title: Aspose.Words per .NET API Reference
description: HtmlFixedSaveOptions proprietà. Specifica i margini attorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o maggiore di 0. Il valore predefinito è 10 punti.
type: docs
weight: 120
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Specifica i margini attorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o maggiore di 0. Il valore predefinito è 10 punti.

```csharp
public double PageMargins { get; set; }
```

### Osservazioni

Dipende dal valore di[`PageHorizontalAlignment`](../pagehorizontalalignment/) proprietà:

* Definisce i margini superiore, inferiore e sinistro della pagina, se il valore lo èLeft .
* Definisce i margini superiore, inferiore e destro della pagina, se il valore lo èRight .
* Definisce i margini superiore e inferiore della pagina se il valore lo èCenter .

### Esempi

Mostra come regolare i margini della pagina quando si salva un documento in HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assemblea [Aspose.Words](../../../)


