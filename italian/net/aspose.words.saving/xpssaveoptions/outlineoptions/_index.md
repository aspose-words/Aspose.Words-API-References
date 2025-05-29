---
title: XpsSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà OutlineOptions di XpsSaveOptions per personalizzare le impostazioni della struttura del tuo documento, migliorandone l'organizzazione e la presentazione.
type: docs
weight: 30
url: /it/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Consente di specificare le opzioni del contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Osservazioni

Notare che[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) l'opzione non funzionerà durante il salvataggio in XPS.

## Esempi

Mostra come limitare il livello delle intestazioni che appariranno nella struttura di un documento XPS salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire titoli che possono fungere da voci di indice dei livelli 1, 2 e poi 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Creiamo un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Il documento XPS di output conterrà una struttura, un indice che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema verremo indirizzati alla posizione della rispettiva intestazione.
// Impostare la proprietà "HeadingsOutlineLevels" su "2" per escludere dalla struttura tutte le intestazioni i cui livelli sono superiori a 2.
// Le ultime due intestazioni che abbiamo inserito sopra non verranno visualizzate.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Guarda anche

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
