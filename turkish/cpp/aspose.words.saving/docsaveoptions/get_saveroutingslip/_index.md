---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip yöntemi"
linktitle: "get_SaveRoutingSlip"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip yöntemi. false olduğunda, RoutingSlip verisi çıktı belgesine kaydedilmez. Varsayılan değer C++'da true'dur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.saving/docsaveoptions/get_saveroutingslip/
---
## DocSaveOptions::get_SaveRoutingSlip method


**false** olduğunda, RoutingSlip verileri çıktı belgesine kaydedilmez. Varsayılan değer **true**dır.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip() const
```


## Örnekler



Eski Microsoft Word formatları için kaydetme seçeneklerini nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Microsoft Word veya Aspose.Words tarafından belgenin yüklenmesini koruyacak bir şifre belirleyin.
// Bu işlemin belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options->set_Password(u"MyPassword");

// Belge bir yönlendirme fişi içeriyorsa, bu bayrağı true olarak ayarlayarak kaydederken koruyabiliriz.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// Belgeyi yükleyebilmek için,
// DocSaveOptions nesnesinde belirttiğimiz şifreyi bir LoadOptions nesnesinde uygulamamız gerekecek.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
