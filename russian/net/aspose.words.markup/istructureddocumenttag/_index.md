---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words для .NET
description: Aspose.Words.Markup.IStructuredDocumentTag интерфейс. Интерфейс для определения общих данных дляStructuredDocumentTag иStructuredDocumentTagRangeStart  на С#.
type: docs
weight: 3970
url: /ru/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Интерфейс для определения общих данных для[`StructuredDocumentTag`](../structureddocumenttag/) и[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Получает или задает цвет тега структурированного документа. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Указывает для этого уникальный постоянный числовой идентификатор, доступный только для чтения.**СДТ**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Указывает, будет ли содержимое этого**СДТ** должно интерпретироваться как содержащее заполнитель text (в отличие от обычного текстового содержимого в SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Получает уровень, на котором это**СДТ** встречается в дереве документа. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Если установлено значение true, это свойство запретит пользователю удалять это**СДТ** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого файла.**СДТ** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Получает[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано через[`XmlMapping`](./xmlmapping/) element или[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) элемент верен. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Получает или задает Имя[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Получает тип этого**Тег структурированного документа** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Указывает тег, связанный с текущим узлом SDT. Не может быть нулевым. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Указывает понятное имя, связанное с этим**СДТ** . Не может быть нулевым. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Получает объект, который представляет сопоставление этого тега структурированного документа с XML-данными в пользовательской части XML текущего документа. |

## Методы

| Имя | Описание |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Возвращает true, если этот экземпляр является тегом структурированного документа с ранжированием. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Возвращает объект Node, реализующий этот интерфейс. |

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
