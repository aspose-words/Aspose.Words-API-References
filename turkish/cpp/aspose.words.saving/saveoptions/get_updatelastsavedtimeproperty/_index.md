---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty metodu"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty metodu. C++'da LastSavedTime özelliğinin kaydetmeden önce güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Kaydetmeden önce [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) özelliğinin güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Örnekler



Kaydetme sırasında belgenin "Last saved time" özelliğinin korunup korunmayacağını nasıl belirleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// Belgeyi OOXML formatında kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgeyi kaydetme yöntemine geçirerek belgeyi nasıl kaydedeceğimizi değiştirebiliriz.
// "UpdateLastSavedTimeProperty" özelliğini "true" olarak ayarlayın
// çıktı belgesinin "Last saved time" yerleşik özelliğini geçerli tarih/saat olarak ayarlayın.
// "UpdateLastSavedTimeProperty" özelliğini "false" olarak ayarlayın
// giriş belgesinin "Last saved time" yerleşik özelliğinin orijinal değerini koruyun.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
