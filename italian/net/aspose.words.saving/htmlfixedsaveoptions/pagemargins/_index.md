---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageMargins di HtmlFixedSaveOptions per personalizzare i margini del tuo documento HTML. Imposta i valori in punti per un controllo preciso del layout.
type: docs
weight: 130
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Specifica i margini attorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o maggiore di 0. Il valore predefinito è 10 punti.

```csharp
public double PageMargins { get; set; }
```

## Osservazioni

Dipende dal valore di[`PageHorizontalAlignment`](../pagehorizontalalignment/) proprietà:

* Definisce i margini di pagina superiore, inferiore e sinistro se il valore èLeft .
* Definisce i margini di pagina superiore, inferiore e destro se il valore èRight .
* Definisce i margini di pagina superiore e inferiore se il valore èCenter .

## Esempi

Mostra come regolare i margini della pagina quando si salva un documento in formato HTML.

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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
