---
title: "Метод Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf"
linktitle: "get_SaveImagesAsWmf"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf. Когда true, все изображения будут сохраняться как WMF в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


Когда **true**, все изображения будут сохранены как WMF.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## Примеры



Показывает, как преобразовать все изображения в документе в формат Windows Metafile при сохранении документа в RTF.
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

// Создайте объект \"RtfSaveOptions\", который передадите методу \"Save\" документа, чтобы изменить способ сохранения его в RTF.
auto rtfSaveOptions = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

// Установите свойство "SaveImagesAsWmf" в "true", чтобы преобразовать все изображения в документе в WMF при сохранении его в RTF.
// Это поможет таким читателям, как WordPad, читать наш документ.
// Установите свойство "SaveImagesAsWmf" в "false", чтобы сохранить оригинальный формат всех изображений в документе
// при сохранении его в RTF. Это сохранит качество изображений ценой совместимости со старыми RTF‑чтителями.
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

## См. также

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
