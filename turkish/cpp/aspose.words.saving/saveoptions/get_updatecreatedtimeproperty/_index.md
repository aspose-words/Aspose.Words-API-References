---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty yöntemi"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty yöntemi. Kaydetmeden önce CreatedTime özelliğinin güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**'dur; C++'da."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


[CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer **false**;

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Örnekler



Kaydederken bir belgenin "CreatedTime" özelliğinin nasıl güncelleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Bu bayrak, yerleşik bir özellik olan oluşturulma zamanının güncellenip güncellenmeyeceğini belirler.
// Eğer öyleyse, belgenin en son kaydetme işleminin tarihi
// Bu SaveOptions nesnesi parametre olarak geçirildiğinde oluşturulma zamanı olarak kullanılır.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Kaydedilen belgeyi açın, ardından özelliğin değerini doğrulayın.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
