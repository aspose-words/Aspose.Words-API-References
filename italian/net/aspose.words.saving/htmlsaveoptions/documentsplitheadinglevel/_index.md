---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words per .NET
description: Ottimizza la suddivisione dei documenti con DocumentSplitHeadingLevel di HtmlSaveOptions. Controlla i livelli delle intestazioni per una migliore organizzazione. Il valore predefinito è 2.
type: docs
weight: 90
url: /it/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Specifica il livello massimo di intestazioni in cui dividere il documento. Il valore predefinito è`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Osservazioni

Quando[`DocumentSplitCriteria`](../documentsplitcriteria/) includeHeadingParagraph e questa proprietà è impostata su un valore da 1 a 9, il documento verrà diviso in paragrafi formattati utilizzando **Titolo 1** ,**Titolo 2** ,**Titolo 3**ecc. stili fino al livello di intestazione specificato.

Per impostazione predefinita, solo**Titolo 1** E**Titolo 2** i paragrafi determinano la divisione del documento. Impostando questa proprietà su zero, il documento non verrà affatto diviso nei paragrafi di intestazione.

## Esempi

Mostra come suddividere un documento HTML di output in più parti tramite intestazioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ogni paragrafo che formattiamo utilizzando uno stile "Titolo" può fungere da titolo.
// Ogni intestazione può anche avere un livello di intestazione, determinato dal numero del suo stile di intestazione.
// Le intestazioni sottostanti si riferiscono ai livelli 1-3.
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

// Crea un oggetto HtmlSaveOptions e imposta il criterio di suddivisione su "HeadingParagraph".
// Questi criteri divideranno il documento in paragrafi con stili "Titolo" in diversi documenti più piccoli,
// e salva ogni documento in un file HTML separato nel file system locale.
// Imposteremo anche il livello massimo dell'intestazione, che divide il documento in 2.
// Salvando il documento, questo verrà diviso in base alle intestazioni di livello 1 e 2, ma non da 3 a 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Il nostro documento ha quattro titoli di livello 1 - 2. Uno di questi titoli non sarà
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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
