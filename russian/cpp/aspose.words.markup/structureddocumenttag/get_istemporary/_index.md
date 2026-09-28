---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary метод"
linktitle: "get_IsTemporary"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary метод. Указывает, будет ли этот SDT удалён из документа WordProcessingML, когда его содержимое изменяется в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Указывает, следует ли удалять этот **SDT** из документа WordProcessingML при изменении его содержимого.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Примеры



Показывает, как создавать одноразовые элементы управления.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте структурированный тег документа простого текста,
// который будет выступать в качестве простой текстовой формы, в которую пользователь может вводить текст.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Установите свойство "IsTemporary" в значение "true", чтобы структурированный тег документа исчез и
// встроить его содержимое в документ после того, как пользователь отредактирует его один раз в Microsoft Word.
// Установите свойство "IsTemporary" в значение "false", чтобы пользователь мог редактировать содержимое
// структурированного тега документа любое количество раз.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Вставьте ещё один структурированный тег документа в виде флажка и установите его состояние по умолчанию в "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Установите свойство "IsTemporary" в значение "true", чтобы флажок превратился в символ
// после того, как пользователь щёлкнет по нему в Microsoft Word.
// Установите свойство "IsTemporary" в значение "false", чтобы пользователь мог щёлкать по флажку любое количество раз.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
