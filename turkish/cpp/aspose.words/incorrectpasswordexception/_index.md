---
title: "Aspose::Words::IncorrectPasswordException typedef"
linktitle: "IncorrectPasswordException"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IncorrectPasswordException typedef. Bir belge bir şifreyle şifrelendiğinde ve belge açılırken belirtilen şifre yanlış veya eksik olduğunda fırlatılır. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 134000
url: /tr/cpp/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException typedef


Bir belge bir şifreyle şifrelenmiş ve belge açılırken belirtilen şifre yanlış veya eksikse fırlatılır. Daha fazla bilgi için [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
using Aspose::Words::IncorrectPasswordException = typedef System::ExceptionWrapper<Details_IncorrectPasswordException>
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
