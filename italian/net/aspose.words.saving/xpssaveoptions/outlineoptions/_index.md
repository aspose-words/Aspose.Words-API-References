---
title: XpsSaveOptions.OutlineOptions
second_title: Aspose.Words per .NET API Reference
description: XpsSaveOptions proprietà. Permette di specificare le opzioni del contorno.
type: docs
weight: 20
url: /it/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Permette di specificare le opzioni del contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Osservazioni

Notare che[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) l'opzione non funzionerà durante il salvataggio su XPS.

### Esempi

Mostra come limitare il livello delle intestazioni che appariranno nella struttura di un documento XPS salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci intestazioni che possono servire come voci di sommario dei livelli 1, 2 e poi 3.
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
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Il documento XPS di output conterrà una struttura, un sommario che elenca le intestazioni nel corpo del documento.
// Facendo clic su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "2" per escludere dalla struttura tutte le intestazioni i cui livelli sono superiori a 2.
// Le ultime due intestazioni che abbiamo inserito sopra non appariranno.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Guarda anche

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../xpssaveoptions/)
* assemblea [Aspose.Words](../../../)


