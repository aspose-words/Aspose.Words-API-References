---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica il livello massimo di intestazioni popolate nella mappa di navigazione durante lesportazione nel formato EPUB IDPF. Il valore predefinito è3 .
type: docs
weight: 110
url: /it/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

Specifica il livello massimo di intestazioni popolate nella mappa di navigazione durante l'esportazione nel formato EPUB IDPF. Il valore predefinito è`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### Osservazioni

La mappa di navigazione in formato EPUB IDPF consente agli interpreti di fornire un modo semplice di navigazione attraverso la struttura del documento. Solitamente i punti di navigazione corrispondono alle intestazioni del documento. Per popolare le intestazioni fino al livello **N** assegnare questo valore a`EpubNavigationMapLevel`.

Per impostazione predefinita, vengono popolati tre livelli di intestazioni: paragrafi di stili **Titolo 1** , **Titolo 2** e **Titolo 3**. È possibile impostare questa proprietà su un valore compreso tra 1 e 9 per richiedere il livello massimo corrispondente. L'impostazione a zero ridurrà la mappa di navigazione solo alla radice del documento o alle radici delle parti del documento.

### Esempi

Mostra come filtrare le intestazioni che appaiono nel pannello di navigazione di un documento Epub salvato.

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

// I lettori di Epub in genere creano un sommario per i loro documenti.
// Ogni paragrafo con uno stile "Titolo" nel documento creerà una voce in questo sommario.
 // Possiamo usare la proprietà "EpubNavigationMapLevel" per impostare un livello di intestazione massimo.
// Il lettore Epub non aggiungerà titoli con un livello superiore a quello specificato nella tabella dei contenuti.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// Il nostro documento ha sei titoli, due dei quali sono al di sopra del livello 2.
// Il sommario di questo documento avrà quattro voci.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


