---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StoryType enum. Текст документа Word хранится в историях. StoryType определяет историю в C++."
type: docs
weight: 117000
url: /ru/cpp/aspose.words/storytype/
---
## StoryType enum


Текст документа Word хранится в историях. [StoryType](./) определяет историю.

```cpp
enum class StoryType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Значение по умолчанию. В документе нет такой истории. |
| MainText | 1 | Содержит основной текст документа, представленный элементом [Body](../body/). |
| Footnotes | 2 | Содержит текст сноски, представленный элементом [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Содержит текст концевой сноски, представленный элементом [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Содержит комментарии документа (аннотации), представленные элементом [Comment](../comment/). |
| Textbox | 5 | Содержит текст формы или текстового поля, представленный элементом [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Содержит текст верхнего колонтитула чётных страниц, представленный элементом [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Содержит текст основного верхнего колонтитула. Когда верхний колонтитул различается для нечётных и чётных страниц, содержит текст верхнего колонтитула нечётных страниц. Представлен элементом [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Содержит текст нижнего колонтитула чётных страниц, представленный элементом [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Содержит текст основного нижнего колонтитула. Когда нижний колонтитул различается для нечётных и чётных страниц, содержит текст нижнего колонтитула нечётных страниц. Представлен элементом [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Содержит текст верхнего колонтитула первой страницы, представленный элементом [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Содержит текст нижнего колонтитула первой страницы, представленный элементом [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Содержит текст разделителя сносок. |
| FootnoteContinuationSeparator | 13 | Содержит текст разделителя продолжения сноски. |
| FootnoteContinuationNotice | 14 | Содержит текст разделителя уведомления о продолжении сноски. |
| EndnoteSeparator | 15 | Содержит текст разделителя сносок. |
| EndnoteContinuationSeparator | 16 | Содержит текст разделителя продолжения сносок. |
| EndnoteContinuationNotice | 17 | Содержит текст разделителя уведомления о продолжении сносок. |


## Примеры



Показывает, как удалить все фигуры из узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте DocumentBuilder для вставки фигуры. Это встроенная фигура,
// которая имеет родительский Paragraph, являющийся дочерним узлом Body первой секции.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Мы можем удалить все фигуры из дочерних абзацев этого Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
