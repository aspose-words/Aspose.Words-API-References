---
title: Enum SdtType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Markup.SdtType перечисление. Указывает тип узла тега структурированного документа SDT.
type: docs
weight: 3800
url: /ru/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Указывает тип узла тега структурированного документа (SDT).

```csharp
public enum SdtType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Тип SDT не назначен. |
| Bibliography | `1` | SDT представляет библиографическую запись. |
| Citation | `2` | SDT представляет цитату. |
| Equation | `3` | SDT представляет уравнение. |
| DropDownList | `4` | SDT представляет собой раскрывающийся список при отображении в документе. |
| ComboBox | `5` | SDT представляет собой поле со списком при отображении в документе. |
| Date | `6` | SDT представляет средство выбора даты при отображении в документе. |
| BuildingBlockGallery | `7` | SDT представляет тип галереи стандартных блоков. |
| DocPartObj | `8` | SDT представляет тип части документа. |
| Group | `9` | SDT представляет ограниченную группу при отображении в документе. |
| Picture | `10` | SDT представляет изображение при отображении в документе. |
| RichText | `11` | SDT представляет собой форматированное текстовое поле при отображении в документе. |
| PlainText | `12` | SDT представляет собой обычное текстовое поле при отображении в документе. |
| Checkbox | `13` | SDT представляет собой флажок при отображении в документе. |
| RepeatingSection | `14` | SDT представляет тип повторяющегося раздела при отображении в документе. |
| RepeatingSectionItem | `15` | SDT представляет элемент повторяющегося раздела. |
| EntityPicker | `16` | SDT представляет средство выбора объектов, которое позволяет пользователю выбирать экземпляр внешнего типа контента. |

### Примеры

Показывает, как работать со стилями для элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля из документа к тегу структурированного документа.
// 1 - Применить объект стиля из коллекции стилей документа:
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

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Показывает, как заполнить таблицу данными из части XML.

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

// Создаем заголовки для данных из содержимого XML.
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

// Добавляем элемент повторяющегося раздела внутри повторяющегося раздела и помечаем его как строку.
// В этой таблице будет строка для каждого элемента, который мы можем найти в XML-документе
// используя XPath "/books[1]/book", которых три.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Сопоставить XML-данные с созданными ячейками таблицы для названия и автора каждой книги.
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


