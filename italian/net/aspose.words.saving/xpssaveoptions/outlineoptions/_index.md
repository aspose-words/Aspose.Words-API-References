---
title: OutlineOptions
second_title: Aspose.Words per .NET API Reference
description: Consente di specificare le opzioni del contorno.
type: docs
weight: 20
url: /it/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Consente di specificare le opzioni del contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Osservazioni

Si noti che l'opzione ExpandedOutlineLevels non funzionerà durante il salvataggio su XPS.

### Esempi

Mostra come limitare il livello delle intestazioni che appariranno nella struttura di un documento XPS salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce intestazioni che possono fungere da voci TOC di livello 1, 2 e poi 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Il documento XPS di output conterrà uno schema, un sommario che elenca i titoli nel corpo del documento.
// Cliccando su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "2" per escludere tutte le intestazioni i cui livelli sono superiori a 2 dalla struttura.
// Le ultime due intestazioni che abbiamo inserito sopra non appariranno.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Guarda anche

* class [OutlineOptions](../../outlineoptions)
* class [XpsSaveOptions](../../xpssaveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../xpssaveoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->