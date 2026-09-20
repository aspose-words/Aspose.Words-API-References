---
title: "Aspose::Words::Saving::DocSaveOptions::get_Password метод"
linktitle: "get_Password"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_Password метод. Получает/устанавливает пароль для шифрования документа с использованием метода шифрования RC4 в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


Получает/устанавливает пароль для шифрования документа методом шифрования RC4.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## Примечания


Чтобы сохранить документ без шифрования, это свойство должно быть **null** или пустой строкой.

## Примеры



Показывает, как задать параметры сохранения для более старых форматов Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Установите пароль, который будет защищать загрузку документа в Microsoft Word или Aspose.Words.
// Обратите внимание, что это никоим образом не шифрует содержимое документа.
options->set_Password(u"MyPassword");

// Если документ содержит маршрутный лист, мы можем сохранить его при сохранении, установив этот флаг в значение true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// Чтобы иметь возможность загрузить документ,
// нам потребуется применить пароль, указанный в объекте DocSaveOptions, в объекте LoadOptions.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
