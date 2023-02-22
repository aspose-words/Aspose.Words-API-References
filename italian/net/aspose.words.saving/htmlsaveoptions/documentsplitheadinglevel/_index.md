---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica il livello massimo di intestazioni a cui dividere il documento. Il valore predefinito è2 .
type: docs
weight: 90
url: /it/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Specifica il livello massimo di intestazioni a cui dividere il documento. Il valore predefinito è`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### Osservazioni

quando[`DocumentSplitCriteria`](../documentsplitcriteria/) includeHeadingParagraph e questa proprietà è impostata su un valore compreso tra 1 e 9, il documento verrà suddiviso in paragrafi formattati utilizzando  **Titolo 1** , **Titolo 2** , **Titolo 3** ecc. stili fino al livello di intestazione specificato.

Per impostazione predefinita, solo **Titolo 1** e **Titolo 2** paragrafi causano la divisione del documento. L'impostazione di questa proprietà su zero farà sì che il documento non venga affatto suddiviso nei paragrafi di intestazione.

### Esempi

Mostra come dividere un documento HTML di output per intestazioni in più parti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ogni paragrafo che formattiamo usando uno stile "Intestazione" può fungere da intestazione.
// Ogni intestazione può anche avere un livello di intestazione, determinato dal numero del suo stile di intestazione.
// I titoli sottostanti sono di livello 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Crea un oggetto HtmlSaveOptions e imposta i criteri di divisione su "HeadingParagraph".
// Questi criteri divideranno il documento in paragrafi con stili "Titolo" in diversi documenti più piccoli,
// e salva ogni documento in un file HTML separato nel file system locale.
// Imposteremo anche il livello di intestazione massimo, che divide il documento su 2.
// Il salvataggio del documento lo dividerà alle intestazioni dei livelli 1 e 2, ma non da 3 a 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Il nostro documento ha quattro titoli di livello 1 - 2. Uno di questi titoli non lo sarà
// un punto di divisione poiché si trova all'inizio del documento.
// L'operazione di salvataggio dividerà il nostro documento in tre punti, in quattro documenti più piccoli.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


