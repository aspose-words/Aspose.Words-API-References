---
title: "Aspose::Words::Saving::DocSaveOptions::DocSaveOptions yapıcı"
linktitle: "DocSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocSaveOptions::DocSaveOptions yapıcı. Bu sınıfın yeni bir örneğini başlatır; C++'da bir belgeyi Doc formatında kaydetmek için kullanılabilir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions::DocSaveOptions() constructor


Bu sınıfın yeni bir örneğini başlatır; bir belgeyi [Doc](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::DocSaveOptions::DocSaveOptions()
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
## DocSaveOptions::DocSaveOptions(Aspose::Words::SaveFormat) constructor


Bu sınıfın yeni bir örneğini başlatır; bir belgeyi [Doc](../../../aspose.words/saveformat/) veya [Dot](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::DocSaveOptions::DocSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | [Doc](../../../aspose.words/saveformat/) veya [Dot](../../../aspose.words/saveformat/) olabilir. |

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
