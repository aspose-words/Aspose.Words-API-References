---
title: "Перечисление Aspose::Words::NodeType"
linktitle: "NodeType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::NodeType. Указывает тип узла документа Word в C++."
type: docs
weight: 102000
url: /ru/cpp/aspose.words/nodetype/
---
## NodeType enum


Указывает тип узла документа Word.

```cpp
enum class NodeType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Any | 0 | Указывает все типы узлов. Позволяет выбрать всех дочерних элементов. |
| Document | 1 | Объект [Document](../document/), который в качестве корня дерева документа предоставляет доступ ко всему документу Word. Узел [Document](../document/) может иметь узлы [Section](../section/). |
| Section | 2 | Объект [Section](../section/), который соответствует одному разделу в документе Word. Узел [Section](../section/) может иметь узлы [Body](../body/) и [HeaderFooter](../headerfooter/). |
| Body | 3 | Объект [Body](../body/), содержащий основной текст раздела (основная текстовая история). Узел [Body](../body/) может иметь узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). |
| HeaderFooter | 4 | Объект [HeaderFooter](../headerfooter/), содержащий текст конкретного верхнего или нижнего колонтитула внутри раздела. Узел [HeaderFooter](../headerfooter/) может иметь узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). |
| Table | 5 | Объект [Table](../../aspose.words.tables/table/), представляющий таблицу в документе Word. Узел [Table](../../aspose.words.tables/table/) может иметь узлы [Row](../../aspose.words.tables/row/). |
| Row | 6 | Строка таблицы. Узел [Row](../../aspose.words.tables/row/) может иметь узлы [Cell](../../aspose.words.tables/cell/). |
| Cell | 7 | Ячейка строки таблицы. Узел [Cell](../../aspose.words.tables/cell/) может иметь узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). |
| Paragraph | 8 | Абзац текста. Узел [Paragraph](../paragraph/) является контейнером для встроенных элементов уровня строки: [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), а также [BookmarkStart](../bookmarkstart/) и [BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | Начало маркера закладки. |
| BookmarkEnd | 10 | Конец маркера закладки. |
| EditableRangeStart | 11 | Начало редактируемого диапазона. |
| EditableRangeEnd | 12 | Конец редактируемого диапазона. |
| MoveFromRangeStart | 13 | Начало диапазона MoveFrom. |
| MoveFromRangeEnd | 14 | Конец диапазона MoveFrom. |
| MoveToRangeStart | 15 | Начало диапазона MoveTo. |
| MoveToRangeEnd | 16 | Конец диапазона MoveTo. |
| GroupShape | 17 | Группа фигур, изображений, OLE‑объектов или других групповых фигур. Узел [GroupShape](../../aspose.words.drawing/groupshape/) может содержать другие узлы [Shape](../../aspose.words.drawing/shape/) и [GroupShape](../../aspose.words.drawing/groupshape/). |
| Shape | 18 | Графический объект, такой как фигура OfficeArt, изображение или OLE‑объект. Узел [Shape](../../aspose.words.drawing/shape/) может содержать узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). |
| Comment | 19 | Комментарий в документе Word. Узел [Comment](../comment/) может иметь узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). |
| Footnote | 20 | Сноска или концевой сноска в документе Word. Узел [Footnote](../../aspose.words.notes/footnote/) может иметь узлы [Paragraph](../paragraph/) и [Table](../../aspose.words.tables/table/). |
| Run | 21 | Последовательность текста. |
| FieldStart | 22 | Специальный символ, обозначающий начало поля Word. |
| FieldSeparator | 23 | Специальный символ, разделяющий код поля и результат поля. |
| FieldEnd | 24 | Специальный символ, обозначающий конец поля Word. |
| FormField | 25 | Поле формы. |
| SpecialChar | 26 | Специальный символ, который не относится к более конкретным типам специальных символов. |
| SmartTag | 27 | Умный тег, охватывающий одну или несколько встроенных структур (последовательности, изображения, поля и т.д.) внутри абзаца. |
| StructuredDocumentTag | 28 | Позволяет определить специфическую для клиента информацию и способы её представления. |
| StructuredDocumentTagRangeStart | 29 | Начало **ranged** структурного тега документа, который принимает контент из нескольких разделов. |
| StructuredDocumentTagRangeEnd | 30 | Конец **ranged** структурного тега документа, который принимает контент из нескольких разделов. |
| GlossaryDocument | 31 | Глоссарийный документ внутри основного документа. |
| BuildingBlock | 32 | Строительный блок внутри глоссарийного документа (например, запись глоссарийного документа). |
| CommentRangeStart | 33 | Маркерный узел, представляющий начало комментируемого диапазона. |
| CommentRangeEnd | 34 | Маркерный узел, представляющий конец комментируемого диапазона. |
| OfficeMath | 35 | Объект Office [Math](../../aspose.words.math/). Может быть уравнением, функцией, матрицей или одним из других математических объектов. Может быть коллекцией математических объектов и также может содержать некоторые нематематические объекты, такие как фрагменты текста. |
| SubDocument | 36 | Узел поддокумента, который является ссылкой на другой документ. |
| System | 37 | Зарезервировано для внутреннего использования [Aspose.Words](../). |
| Null | 38 | Зарезервировано для внутреннего использования [Aspose.Words](../). |


## Примеры



Показывает, как пройтись по коллекции дочерних узлов составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Добавьте два фрагмента текста и одну фигуру в качестве дочерних узлов к первому абзацу этого документа.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Обратите внимание, что 'CustomNodeId' не сохраняется в выходной файл и существует только в течение жизни узла.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Итерируйтесь по коллекции непосредственных дочерних элементов абзаца,
// и выводите любые фрагменты текста или фигуры, которые мы находим внутри.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
