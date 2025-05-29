---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words per .NET
description: Ottimizza le dimensioni dei documenti RTF con la proprietà ExportCompactSize. Garantisci un'archiviazione efficiente mantenendo l'integrità del testo, anche con contenuti RTL.
type: docs
weight: 20
url: /it/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Consente di ridurre le dimensioni dei documenti RTF in output, ma se contengono testo RTL (da destra a sinistra), non verrà visualizzato correttamente. Il valore predefinito è`falso` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Osservazioni

Se il documento che si desidera convertire in RTF utilizzando Aspose.Words non contiene testo da destra a sinistra in lingue come l'arabo, è possibile impostare questa opzione su`VERO` per ridurre la dimensione del file RTF risultante.

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

* class [RtfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
