---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate метод"
linktitle: "get_DefaultTemplate"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate метод. Получает или задаёт путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — пустая строка в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


## Примеры



Показывает, как установить шаблон по умолчанию для документов, у которых нет прикреплённых шаблонов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Включите автоматическое обновление стилей, но не прикрепляйте документ шаблона.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Поскольку шаблонного документа нет, у документа не было места для отслеживания изменений стилей.
// Используйте объект SaveOptions, чтобы автоматически установить шаблон
// если документ, который мы сохраняем, не имеет его.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
