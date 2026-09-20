---
title: "Метод Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl"
linktitle: "get_LockContentControl"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl. При установке в true это свойство запрещает пользователю удалять этот **SDT** в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_lockcontentcontrol/
---
## StructuredDocumentTag::get_LockContentControl method


Если установлено в **true**, это свойство запретит пользователю удалять этот **SDT**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl() override
```


## Примеры



Показывает, как применять ограничения редактирования к структурированным тегам документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте простой текстовый структурированный тег документа, который действует как текстовое поле, предлагающее пользователю заполнить его.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Установите свойство "LockContents" в значение "true", чтобы запретить пользователю редактировать содержимое этого текстового поля.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Установите свойство "LockContentControl" в значение "true", чтобы запретить пользователю
// удалять этот структурированный тег документа вручную в Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
