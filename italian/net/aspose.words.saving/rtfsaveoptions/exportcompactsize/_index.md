---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words per .NET API Reference
description: RtfSaveOptions proprietà. Consente di ridurre le dimensioni dei documenti RTF di output ma se contengono testo RTL da destra a sinistra non verrà visualizzato correttamente. Il valore predefinito èfalso .
type: docs
weight: 20
url: /it/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Consente di ridurre le dimensioni dei documenti RTF di output, ma se contengono testo RTL (da destra a sinistra), non verrà visualizzato correttamente. Il valore predefinito è`falso` .

```csharp
public bool ExportCompactSize { get; set; }
```

### Osservazioni

Se il documento che desideri convertire in RTF utilizzando Aspose.Words non contiene testo da destra a sinistra in lingue come l'arabo, puoi impostare questa opzione su`VERO` per ridurre la dimensione dell'RTF risultante.

### Esempi

Mostra come salvare un documento in formato .rtf con opzioni personalizzate.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un oggetto "RtfSaveOptions" da passare al metodo "Save" del documento per modificare il modo in cui lo salviamo in un RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Imposta la proprietà "ExportCompactSize" su "true" su
// riduce le dimensioni del documento salvato a scapito della compatibilità del testo da destra a sinistra.
options.ExportCompactSize = true;

// Imposta la proprietà "ExportImagesFotOldReaders" su "true" per utilizzare parole chiave aggiuntive per garantire che il nostro documento sia
// compatibile con lettori di versioni precedenti a Microsoft Word 97 e WordPad.
// Imposta la proprietà "ExportImagesFotOldReaders" su "false" per ridurre la dimensione del documento,
// ma impedisce ai vecchi lettori di leggere qualsiasi immagine non metafile o BMP che il documento potrebbe contenere.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Guarda anche

* class [RtfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../rtfsaveoptions/)
* assemblea [Aspose.Words](../../../)


