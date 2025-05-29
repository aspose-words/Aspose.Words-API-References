---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Markup.SdtType, определяющее структурированные типы тегов документов для улучшенного управления документами и оптимизированных рабочих процессов.
type: docs
weight: 4730
url: /ru/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Указывает тип узла структурированного тега документа (SDT).

```csharp
public enum SdtType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Тип SDT не назначен. |
| Bibliography | `1` | SDT представляет собой библиографическую запись. |
| Citation | `2` | SDT представляет собой цитату. |
| Equation | `3` | SDT представляет собой уравнение. |
| DropDownList | `4` | При отображении в документе SDT представляет собой раскрывающийся список. |
| ComboBox | `5` | При отображении в документе SDT представляет собой поле со списком. |
| Date | `6` | SDT представляет собой средство выбора даты при отображении в документе. |
| BuildingBlockGallery | `7` | SDT представляет собой тип галереи строительных блоков. |
| DocPartObj | `8` | SDT представляет собой тип части документа. |
| Group | `9` | SDT представляет собой ограниченную группировку при отображении в документе. |
| Picture | `10` | SDT представляет собой изображение при отображении в документе. |
| RichText | `11` | SDT представляет собой поле форматированного текста при отображении в документе. |
| PlainText | `12` | При отображении в документе SDT представляет собой простое текстовое поле. |
| Checkbox | `13` | SDT представляет собой флажок при отображении в документе. |
| RepeatingSection | `14` | SDT представляет собой повторяющийся тип раздела при отображении в документе. |
| RepeatingSectionItem | `15` | SDT представляет собой повторяющийся элемент раздела. |
| EntityPicker | `16` | SDT представляет собой средство выбора сущностей, позволяющее пользователю выбирать экземпляр внешнего типа контента. |

## Примеры

Показывает, как создать структурированный тег документа типа «Цитата».

```csharp
Document doc = new Document();

StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.Citation, MarkupLevel.Inline);
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
paragraph.AppendChild(sdt);

// Создать поле «Цитата».
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToParagraph(0, -1);
builder.InsertField(@"CITATION Ath22 \l 1033 ", "(John Lennon, 2022)");

// Переместить поле в тег структурированного документа.
while (sdt.NextSibling != null)
    sdt.AppendChild(sdt.NextSibling);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Citation.docx");
```

Показывает, как создать групповой структурированный тег документа на уровне строки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Создать групповой структурированный тег документа на уровне строки.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Создаем дочернюю строку структурированного тега документа.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Вставить содержимое ячейки.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// Вставьте текст после таблицы.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

Показывает, как работать со стилями для элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля из документа к структурированному тегу документа.
// 1 — Применить объект стиля из коллекции стилей документа:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Ссылка на стиль в документе по имени:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Показывает, как заполнить таблицу данными из XML-части.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// Создаем заголовки для данных из XML-контента.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// Создаем таблицу с повторяющимся разделом внутри.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Добавляем повторяющийся элемент раздела внутрь повторяющегося раздела и отмечаем его как строку.
// Эта таблица будет иметь строку для каждого элемента, который мы можем найти в XML-документе
// с использованием XPath "/books[1]/book", которых существует три.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Сопоставьте XML-данные с созданными ячейками таблицы для названия и автора каждой книги.
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
