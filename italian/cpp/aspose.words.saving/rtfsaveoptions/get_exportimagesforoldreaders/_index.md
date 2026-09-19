---
title: "Metodo Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders. Specifica se le parole chiave per \\\"old readers\\\" sono scritte nel RTF o meno. Questo può influire significativamente sulla dimensione del documento RTF. Il valore predefinito è true in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


Specifica se le parole chiave per "old readers" vengono scritte nel RTF o meno. Questo può influire significativamente sulla dimensione del documento RTF. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Note


\"Old readers\" sono applicazioni precedenti a Microsoft Word 97 e anche WordPad. Quando questa opzione è **true** Aspose.Words scrive parole chiave RTF aggiuntive. Queste parole chiave consentono al documento di essere visualizzato correttamente quando aperto in un'applicazione \"old reader\", ma possono aumentare significativamente la dimensione del documento.

Se imposti questa opzione su **false**, allora solo le immagini nei formati WMF, EMF e BMP saranno visualizzate in \"old readers\".

## Esempi



Mostra come salvare un documento in .rtf con opzioni personalizzate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Crea un oggetto "RtfSaveOptions" da passare al metodo "Save" del documento per modificare il modo in cui lo salviamo in RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Imposta la proprietà "ExportCompactSize" su "true" per
// ridurre le dimensioni del documento salvato a scapito della compatibilità con il testo da destra a sinistra.
options->set_ExportCompactSize(true);

// Imposta la proprietà "ExportImagesFotOldReaders" su "true" per utilizzare parole chiave aggiuntive per garantire che il nostro documento sia
// compatibile con i lettori pre-Microsoft Word 97 e WordPad.
// Imposta la proprietà "ExportImagesFotOldReaders" su "false" per ridurre le dimensioni del documento,
// ma impedisce ai lettori più vecchi di poter leggere eventuali immagini non metafile o BMP che il documento potrebbe contenere.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## Vedi anche

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
