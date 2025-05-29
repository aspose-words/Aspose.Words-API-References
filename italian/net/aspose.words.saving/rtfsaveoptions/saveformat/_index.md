---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveFormat di RtfSaveOptions per salvare senza sforzo i tuoi documenti in formato RTF, garantendo compatibilità e facile condivisione.
type: docs
weight: 40
url: /it/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Esempi

Mostra come salvare un documento in formato .rtf con opzioni personalizzate.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un oggetto "RtfSaveOptions" da passare al metodo "Save" del documento per modificare il modo in cui lo salviamo in un file RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Imposta la proprietà "ExportCompactSize" su "true" per
// riduce le dimensioni del documento salvato a scapito della compatibilità del testo da destra a sinistra.
options.ExportCompactSize = true;

// Imposta la proprietà "ExportImagesFotOldReaders" su "true" per utilizzare parole chiave extra per garantire che il nostro documento sia
// compatibile con i lettori Word 97 precedenti a Microsoft Word e WordPad.
// Impostare la proprietà "ExportImagesFotOldReaders" su "false" per ridurre le dimensioni del documento,
// ma impedisce ai vecchi lettori di leggere eventuali immagini non metafile o BMP contenute nel documento.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
