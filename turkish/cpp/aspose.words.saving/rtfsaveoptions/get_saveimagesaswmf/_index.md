---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf yöntemi"
linktitle: "get_SaveImagesAsWmf"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf yöntemi. **true** olduğunda tüm görüntüler C++'ta WMF olarak kaydedilir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


**true** olduğunda tüm görüntüler WMF olarak kaydedilir.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## Örnekler



Bir belgeyi RTF olarak kaydederken tüm görüntüleri Windows Metafile formatına dönüştürmeyi gösterir.
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

// Bir "RtfSaveOptions" nesnesi oluşturup belgeye ait "Save" yöntemine geçirerek, RTF olarak nasıl kaydedileceğini değiştirebiliriz.
auto rtfSaveOptions = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

// "SaveImagesAsWmf" özelliğini "true" olarak ayarlayın, böylece belge içindeki tüm görüntüler RTF'ye kaydederken WMF'ye dönüştürülür.
// Böyle yapmak, WordPad gibi okuyucuların belgemizi okumasına yardımcı olur.
// "SaveImagesAsWmf" özelliğini "false" olarak ayarlayın, böylece belgedeki tüm görüntülerin özgün formatı korunur
// RTF'ye kaydederken. Bu, görüntü kalitesini korur ancak eski RTF okuyucularıyla uyumluluk pahasına olur.
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

## Ayrıca Bakınız

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
