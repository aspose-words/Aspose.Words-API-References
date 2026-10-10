---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty yöntemi"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty yöntemi. C++'ta LastPrinted özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


[LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Örnekler



Kaydedilirken bir belgenin "Last printed" (Son yazdırılan) özelliğinin nasıl güncelleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Bu bayrak, yerleşik bir özellik olan son yazdırma tarihinin güncellenip güncellenmeyeceğini belirler.
// Eğer öyleyse, belgenin en son kaydetme işleminin tarihi
// bu SaveOptions nesnesi parametre olarak geçirildiğinde yazdırma tarihi olarak kullanılır.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// Microsoft Word 2003'te bu özellik Dosya -> Özellikler -> İstatistikler -> Yazdırıldı yoluyla bulunabilir.
// Belgenin gövdesinde bir PRINTDATE alanı kullanılarak da görüntülenebilir.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Kaydedilen belgeyi açın, ardından özelliğin değerini doğrulayın.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
