---
title: "Aspose::Words::Document::get_AutomaticallyUpdateStyles метод"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_AutomaticallyUpdateStyles. Получает или задает флаг, указывающий, обновляются ли стили в документе, чтобы соответствовать стилям во вложенном шаблоне каждый раз при открытии документа в MS Word на C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Получает или задаёт флаг, указывающий, обновляются ли стили в документе для соответствия стилям прикреплённого шаблона каждый раз при открытии документа в MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Примеры



Показывает, как прикрепить шаблон к документу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Документы Microsoft Word по умолчанию поставляются с прикреплённым шаблоном под названием "Normal.dotm".
// Для пустых документов Aspose.Words нет шаблона по умолчанию.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Прикрепите шаблон, затем установите флаг, чтобы применить изменения стилей
// внутри шаблона к стилям в нашем документе.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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
