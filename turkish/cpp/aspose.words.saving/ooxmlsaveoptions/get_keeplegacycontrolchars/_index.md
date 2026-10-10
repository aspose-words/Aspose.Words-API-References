---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars metodu"
linktitle: "get_KeepLegacyControlChars"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars metodu. C++'da eski kontrol karakterlerinin orijinal temsilini korur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


Eski kontrol karakterlerinin özgün temsilini korur.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Örnekler



.docx'e dönüştürürken eski kontrol karakterlerini nasıl destekleyeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Belgeyi OOXML formatında kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgeyi kaydetme yöntemine geçirerek belgeyi nasıl kaydedeceğimizi değiştirebiliriz.
// \"KeepLegacyControlChars\" özelliğini \"true\" olarak ayarlayın, korumak için
// kaydetme sırasında \"ShortDateTime\" eski karakterini.
// \"KeepLegacyControlChars\" özelliğini \"false\" olarak ayarlayın, kaldırmak için
// çıktı belgesinden \"ShortDateTime\" eski karakterini.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Ayrıca Bakınız

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
