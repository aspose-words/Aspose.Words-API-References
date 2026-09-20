---
title: "Aspose::Words::Document::get_AttachedTemplate метод"
linktitle: "get_AttachedTemplate"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_AttachedTemplate метод. Получает или задает полный путь к шаблону, прикреплённому к документу, в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Получает или задаёт полный путь к шаблону, прикреплённому к документу.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Примечания


Пустая строка означает, что документ привязан к шаблону Normal.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
