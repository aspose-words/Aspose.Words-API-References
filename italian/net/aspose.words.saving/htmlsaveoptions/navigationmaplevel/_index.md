---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words per .NET
description: Scopri la proprietà NavigationMapLevel di HtmlSaveOptions, che controlla i livelli dei titoli nelle esportazioni EPUB, MOBI e AZW3. Massimizza la visibilità dei tuoi contenuti!
type: docs
weight: 390
url: /it/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Specifica il livello massimo di intestazioni da inserire nella mappa di navigazione durante l'esportazione nei formati EPUB, MOBI o AZW3 . Il valore predefinito è`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Osservazioni

La mappa di navigazione consente agli user agent di fornire un modo semplice per navigare attraverso la struttura del documento. Di solito, i punti di navigazione corrispondono alle intestazioni del documento. Per popolare le intestazioni fino al livello**N** assegna questo valore a`NavigationMapLevel`.

Per impostazione predefinita, vengono popolati tre livelli di intestazioni: paragrafi di stili**Titolo 1** ,**Titolo 2** e**Titolo 3**. È possibile impostare questa proprietà su un valore compreso tra 1 e 9 per richiedere il livello massimo corrispondente. Impostandola su zero, la mappa di navigazione verrà ridotta solo alla radice del documento o alle radici delle parti del documento.

## Esempi

Mostra come generare un indice per i documenti Azw3.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Mostra come generare un indice per i documenti Mobi.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Mostra come filtrare le intestazioni che appaiono nel pannello di navigazione di un documento Epub salvato.

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

// Solitamente i lettori di ePub creano un indice per i loro documenti.
// Ogni paragrafo con uno stile "Titolo" nel documento creerà una voce in questo indice.
 // Possiamo usare la proprietà "NavigationMapLevel" per impostare un livello massimo di intestazione.
// Il lettore Epub non aggiungerà titoli con un livello superiore a quello specificato nella tabella dei contenuti.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// Il nostro documento ha sei titoli, due dei quali sono superiori al livello 2.
// L'indice di questo documento conterrà quattro voci.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
