---
title: "Metodo Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf"
linktitle: "get_SaveImagesAsWmf"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf. Quando è true tutte le immagini saranno salvate come WMF in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


Quando **true** tutte le immagini saranno salvate come WMF.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## Esempi



Mostra come convertire tutte le immagini in un documento nel formato Windows Metafile mentre salviamo il documento come RTF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jpeg image:");
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imageShape->get_ImageData()->get_ImageType());

builder->InsertParagraph();
builder->Writeln(u"Png image:");
imageShape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, imageShape->get_ImageData()->get_ImageType());

// Crea un oggetto "RtfSaveOptions" da passare al metodo "Save" del documento per modificare il modo in cui lo salviamo in RTF.
auto rtfSaveOptions = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

// Imposta la proprietà \"SaveImagesAsWmf\" su \"true\" per convertire tutte le immagini nel documento in WMF mentre lo salviamo in RTF.
// In questo modo i lettori come WordPad potranno leggere il nostro documento.
// Imposta la proprietà \"SaveImagesAsWmf\" su \"false\" per preservare il formato originale di tutte le immagini nel documento
// mentre lo salviamo in RTF. Questo preserverà la qualità delle immagini a scapito della compatibilità con i lettori RTF più vecchi.
rtfSaveOptions->set_SaveImagesAsWmf(saveImagesAsWmf);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf");

System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

if (saveImagesAsWmf)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
```

## Vedi anche

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
