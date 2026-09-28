---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag метод"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag метод. Перемещает курсор к структурному тегу документа в C++."
type: docs
weight: 61000
url: /ru/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Перемещает курсор к структурному тегу документа.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | Структурный тег документа, к которому нужно переместиться. |
| characterIndex | int32_t | Индекс символа внутри структурного тега документа. Отрицательное значение позволяет указать позицию от конца структурного тега документа. Используйте -1, чтобы переместиться в конец структурного тега документа. Если структурный тег документа находится на уровне блока и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

## Примеры



Показывает, как переместить курсор [DocumentBuilder](../) внутри структурного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует несколько способов перемещения курсора:
// 1 -  Перейти к первому символу структурированного тега документа по индексу.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Перейти к первому символу структурированного тега документа по объекту.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Перейти к концу второго структурированного тега документа.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Получить текущий выбранный структурированный тег документа.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## См. также

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Перемещает курсор к структурному тегу документа в текущем разделе.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | Индекс структурированного тега документа, к которому нужно переместиться. |
| characterIndex | int32_t | Индекс символа внутри структурного тега документа. Отрицательное значение позволяет указать позицию от конца структурного тега документа. Используйте -1, чтобы переместиться в конец структурного тега документа. Если структурный тег документа находится на уровне блока и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |
## Примечания


Навигация выполняется внутри текущей истории текущего раздела. То есть, если вы переместили курсор к основному заголовку первого раздела, то *structuredDocumentTagIndex* указывает индекс структурированного тега документа внутри этого заголовка данного раздела.

Когда *structuredDocumentTagIndex* больше или равен 0, он указывает индекс от начала раздела, где 0 — первый структурированный тег документа. Когда *structuredDocumentTagIndex* меньше 0, он указывает индекс от конца раздела, где -1 — последний структурированный тег документа.

## Примеры



Показывает, как переместить курсор [DocumentBuilder](../) внутри структурного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует несколько способов перемещения курсора:
// 1 -  Перейти к первому символу структурированного тега документа по индексу.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Перейти к первому символу структурированного тега документа по объекту.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Перейти к концу второго структурированного тега документа.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Получить текущий выбранный структурированный тег документа.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
