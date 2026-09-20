---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph метод"
linktitle: "MoveToParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph метод. Перемещает курсор к абзацу в текущем разделе на C++."
type: docs
weight: 59000
url: /ru/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Перемещает курсор к абзацу в текущем разделе.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraphIndex | int32_t | Индекс абзаца, к которому нужно переместиться. |
| characterIndex | int32_t | Индекс символа внутри абзаца. Отрицательное значение позволяет указать позицию от конца абзаца. Используйте -1, чтобы переместиться в конец абзаца. |
## Примечания


Навигация выполняется внутри текущей истории текущего раздела. То есть, если вы переместили курсор к основному заголовку первого раздела, то *paragraphIndex* указывает индекс абзаца внутри этого заголовка этого раздела.

Когда *paragraphIndex* больше или равен 0, он указывает индекс от начала раздела, где 0 — первый абзац. Когда *paragraphIndex* меньше 0, он указывает индекс от конца раздела, где -1 — последний абзац.

## Примеры



Показывает, как переместить позицию курсора построителя к указанному абзацу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Создайте документный построитель для редактирования документа. Курсор построителя,
// который является точкой, где он будет вставлять новые узлы при вызове его методов построения документа,
// в данный момент находится в начале документа.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Перемещение этого курсора к другому абзацу разместит курсор перед этим абзацем.
builder->MoveToParagraph(2, 0);

// Любой новый контент, который мы добавим, будет вставлен в этой точке.
builder->Writeln(u"This is a new third paragraph. ");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
