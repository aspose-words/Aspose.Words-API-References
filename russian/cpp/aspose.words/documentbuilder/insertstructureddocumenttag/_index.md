---
title: "Метод Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag"
linktitle: "InsertStructuredDocumentTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag. Вставляет StructuredDocumentTag в документ на C++."
type: docs
weight: 46500
url: /ru/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Вставляет [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) в документ.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

Узел [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) только что вставлен.

## Примеры



Показывает, как просто вставить структурный тег документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Обратите внимание, что для вставки разрешены только следующие типы StructuredDocumentTag:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Уровень разметки вставленного StructuredDocumentTag будет определён автоматически и зависит от позиции вставки.
// Добавленный StructuredDocumentTag унаследует форматирование абзаца и шрифта из позиции курсора.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## См. также

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
