---
title: Class ViewOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Settings.ViewOptions classe. Fornisce varie opzioni che controllano la modalità di visualizzazione di un documento in Microsoft Word.
type: docs
weight: 5650
url: /it/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Fornisce varie opzioni che controllano la modalità di visualizzazione di un documento in Microsoft Word.

```csharp
public class ViewOptions
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Controlla la visualizzazione della forma dello sfondo nella vista layout di stampa. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Disattiva la visualizzazione dello spazio tra la parte superiore del testo e il bordo superiore della pagina. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Specifica se il documento è in modalità progettazione moduli. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Controlla la modalità di visualizzazione in Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Ottiene o imposta la percentuale (tra 10 e 500) alla quale si desidera visualizzare il documento. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Ottiene o imposta un valore di zoom in base alle dimensioni della finestra. |

### Esempi

Mostra come impostare un fattore di zoom personalizzato, che le versioni precedenti di Microsoft Word applicheranno a un documento al momento del caricamento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Mostra come impostare un tipo di zoom personalizzato, che le versioni precedenti di Microsoft Word applicheranno a un documento al momento del caricamento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Imposta la proprietà "ZoomType" su "ZoomType.PageWidth" per ottenere Microsoft Word
// per ingrandire automaticamente il documento per adattarlo alla larghezza della pagina.
// Imposta la proprietà "ZoomType" su "ZoomType.FullPage" per ottenere Microsoft Word
// per ingrandire automaticamente il documento per rendere visibile l'intera prima pagina.
// Imposta la proprietà "ZoomType" su "ZoomType.TextFit" per ottenere Microsoft Word
// per ingrandire automaticamente il documento per adattarlo ai margini interni del testo della prima pagina.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Guarda anche

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)


