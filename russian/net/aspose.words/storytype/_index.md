---
title: Enum StoryType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.StoryType перечисление. Текст документа Word хранится в историях. StoryType определяет историю.
type: docs
weight: 5820
url: /ru/net/aspose.words/storytype/
---
## StoryType enumeration

Текст документа Word хранится в историях. **StoryType** определяет историю.

```csharp
public enum StoryType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Значение по умолчанию. В документе такой истории нет. |
| MainText | `1` | Содержит основной текст документа, представленный[`Body`](../body/) . |
| Footnotes | `2` | Содержит текст сноски, представленный[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Содержит текст концевых сносок, представленный[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Содержит комментарии к документу (аннотации), представленные[`Comment`](../comment/) . |
| Textbox | `5` | Содержит фигуру или текст текстового поля, представленный[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Содержит текст заголовка четных страниц, представленный[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Содержит текст основного заголовка. Когда заголовок отличается для нечетных и четных страниц, содержит текст заголовка нечетных страниц. Представлена[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Содержит текст нижнего колонтитула четных страниц, представленный[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Содержит текст основного нижнего колонтитула. Когда нижний колонтитул отличается для нечетных и четных страниц, содержит текст нижнего колонтитула нечетных страниц. Представлена[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Содержит текст заголовка первой страницы, представленный[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Содержит текст нижнего колонтитула первой страницы, представленный[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Содержит текст разделителя сносок, представленныйFootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | Содержит текст разделителя продолжения сноски, представленныйFootnoteSeparator . |
| FootnoteContinuationNotice | `14` | Содержит текст разделителя уведомлений о продолжении сноски, представленныйFootnoteSeparator . |
| EndnoteSeparator | `15` | Содержит текст разделителя концевой сноски, представленныйFootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | Содержит текст разделителя продолжения концевой сноски, представленныйFootnoteSeparator . |
| EndnoteContinuationNotice | `17` | Содержит текст разделителя уведомления о продолжении концевой сноски, представленныйFootnoteSeparator . |

### Примеры

Показывает, как удалить все фигуры из узла.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте DocumentBuilder для вставки фигуры. Это встроенная форма,
// у которого есть родительский абзац, который является дочерним узлом тела первого раздела.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Мы можем удалить все фигуры из дочерних абзацев этого тела.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


