---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password metodu"
linktitle: "get_Password"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password metodu. Belgeyi ECMA376 Standard şifreleme algoritması kullanarak şifrelemek için bir şifre alır/ayarlar C++'da."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Belgeyi ECMA376 Standard şifreleme algoritmasıyla şifrelemek için bir parolayı alır/ayarlar.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Açıklamalar


Belgeyi şifrelemeden kaydetmek için bu özellik **null** veya boş bir dize olmalıdır.

## Örnekler



Şifreyle şifrelenmiş Office Open XML belgesinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// Bu belgeyi Microsoft Word ile ya da
// Aspose.Words doğru şifre sağlanmadan açılamaz.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Şifreli belgeyi doğru şifreyi bir LoadOptions nesnesine geçirerek açın.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
