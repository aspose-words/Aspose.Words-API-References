---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi documenti RTF con la proprietà ExportImagesForOldReaders. Controlla l'inclusione di parole chiave per i lettori legacy, influendo sulle dimensioni e sulle prestazioni dei file.
type: docs
weight: 30
url: /it/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Specifica se le parole chiave per "vecchi lettori" vengono scritte in formato RTF o meno. Ciò può influire significativamente sulla dimensione del documento RTF. Il valore predefinito è`VERO` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Osservazioni

I "vecchi lettori" sono applicazioni precedenti a Microsoft Word 97 e anche WordPad. Quando questa opzione è`VERO` Aspose.Words scrive parole chiave RTF aggiuntive. Queste parole chiave consentono di visualizzare correttamente il documento quando viene aperto in un'applicazione "vecchio lettore" , ma possono aumentare significativamente le dimensioni del documento.

Se imposti questa opzione su`falso`nei "vecchi lettori" verranno visualizzate solo le immagini nei formati WMF, EMF e BMP .

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
