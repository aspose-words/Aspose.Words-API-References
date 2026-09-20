---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password метод"
linktitle: "get_Password"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password метод. Получает/устанавливает пароль для шифрования документа с использованием алгоритма шифрования стандарта ECMA376 в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Получает/задает пароль для шифрования документа с использованием алгоритма шифрования ECMA376 Standard.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Примечания


Чтобы сохранить документ без шифрования, это свойство должно быть **null** или пустой строкой.

## Примеры



Показывает, как создать зашифрованный паролем документ Office Open XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// Мы не сможем открыть этот документ с помощью Microsoft Word или
// Aspose.Words без предоставления правильного пароля.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Откройте зашифрованный документ, передав правильный пароль в объект LoadOptions.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
