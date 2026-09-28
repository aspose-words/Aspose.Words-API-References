---
title: "Aspose::Words::IncorrectPasswordException typedef"
linktitle: "IncorrectPasswordException"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IncorrectPasswordException typedef. Выбрасывается, если документ зашифрован паролем, а указанный при открытии документа пароль неверен или отсутствует. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 134000
url: /ru/cpp/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException typedef


Выбрасывается, если документ зашифрован паролем, а указанный при открытии документа пароль неверен или отсутствует. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::IncorrectPasswordException = typedef System::ExceptionWrapper<Details_IncorrectPasswordException>
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
