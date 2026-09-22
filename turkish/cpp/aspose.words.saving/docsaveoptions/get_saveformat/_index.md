---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveFormat metodu"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveFormat metodu. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin hangi formatta kaydedileceğini belirtir. C++'ta Doc veya Dot olabilir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/docsaveoptions/get_saveformat/
---
## DocSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği formatı belirtir. [Doc](../../../aspose.words/saveformat/) veya [Dot](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DocSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
