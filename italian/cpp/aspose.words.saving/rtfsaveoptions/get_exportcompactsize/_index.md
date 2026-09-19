---
title: "Metodo Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize"
linktitle: "get_ExportCompactSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize. Consente di ridurre le dimensioni dei documenti RTF di output, ma se contengono testo RTL (right-to-left), non verrà visualizzato correttamente. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Consente di rendere i documenti RTF di output più piccoli in dimensione, ma se contengono testo RTL (right-to-left), non verrà visualizzato correttamente. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Note


Se il documento che desideri convertire in RTF usando Aspose.Words non contiene testo da destra a sinistra in lingue come l'arabo, puoi impostare questa opzione su **true** per ridurre le dimensioni del RTF risultante.

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
