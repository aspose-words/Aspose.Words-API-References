---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words для .NET
description: Изучите интерфейс Aspose.Words.Markup.IStructuredDocumentTag для эффективного управления структурированными тегами документов и улучшите обработку документов уже сегодня!
type: docs
weight: 4660
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
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Возвращает или задает внешний вид структурированного тега документа. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Получает или задает цвет структурированного тега документа. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Указывает уникальный постоянный числовой идентификатор, доступный только для чтения, для этого**СДТ**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Возвращает значение true, если этот экземпляр является ранжированным (многосекционным) структурированным тегом документа. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Указывает, является ли содержимое этого**СДТ** должно интерпретироваться как содержащее заполнитель text (в отличие от обычного текстового содержимого в SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Получает уровень, на котором это**СДТ** встречается в дереве документа. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Если установлено значение true, это свойство запретит пользователю удалять этот**СДТ** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Если установлено значение true, это свойство запретит пользователю редактировать содержимое этого**СДТ** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Возвращает объект Node, реализующий этот интерфейс. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Получает[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный элемент XML пуст, как указано через[`XmlMapping`](./xmlmapping/) element или[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) элемент истинен. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Получает или задает имя[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Получает тип этого**Структурированный тег документа** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Указывает тег, связанный с текущим узлом SDT. Не может быть пустым. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Указывает понятное имя, связанное с этим**СДТ** . Не может быть нулевым. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Получает объект, представляющий сопоставление этого структурированного тега документа с XML-данными в пользовательской XML-части текущего документа. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанным типам. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Удаляет только сам узел SDT, но сохраняет его содержимое внутри дерева документа. |

## Примеры

Показывает, как удалить структурированный тег документа, но сохранить содержимое внутри.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Эта коллекция предоставляет унифицированный интерфейс для доступа к ранжированным и неранжированным структурированным тегам.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Здесь мы можем получить дочерние узлы из общего интерфейса ранжированных и неранжированных структурированных тегов.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
