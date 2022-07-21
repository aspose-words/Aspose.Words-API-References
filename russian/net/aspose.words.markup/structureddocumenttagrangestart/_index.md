---
title: StructuredDocumentTagRangeStart
second_title: Справочник по API Aspose.Words для .NET
description: Представляет начало дальнобойный тег структурированного документа который принимает содержимое из нескольких разделов. См. такжеStructuredDocumentTagRangeEnd./structureddocumenttagrangeend .
type: docs
weight: 3850
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Представляет начало **дальнобойный** тег структурированного документа, который принимает содержимое из нескольких разделов. См. также[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend) .

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart)(DocumentBase, SdtType) | Инициализирует новый экземпляр **Начало диапазона тегов структурированного документа** класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes) { get; } | Получает все узлы между начальным узлом диапазона и конечным узлом диапазона. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color) { get; set; } | Получает или задает цвет тега структурированного документа. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит этот узел. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id) { get; } | Указывает уникальный постоянный числовой идентификатор только для чтения для этого тега структурированного документа. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Возвращает true, если этот узел может содержать другие узлы. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext) { get; set; } | Указывает, должно ли содержимое этого тега структурированного документа интерпретироваться как текст-заполнитель (в отличие от обычного текстового содержимого в теге структурированного документа). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild) { get; } | Получает последний дочерний элемент в диапазоне stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level) { get; } | Получает уровень, на котором этот диапазон тегов структурированного документа начинается в дереве документа. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol) { get; set; } | Если установлено значение true, это свойство запрещает пользователю удалять этот тег структурированного документа. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents) { get; set; } | Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого тега структурированного документа. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder) { get; } | Получает[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого тега структурированного документа пусто, связанный отображаемый элемент XML пуст, как указано через[`XmlMapping`](./xmlmapping) элемент или[`IsShowingPlaceholderText`](./isshowingplaceholdertext) элемент истинный. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername) { get; set; } | Получает или задает имя[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) содержащий текст-заполнитель. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend) { get; } | Указывает конец диапазона, если StructuredDocumentTag является ранжированным тегом структурированного документа. В противном случае возвращает null. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype) { get; } | Получает тип тега этого структурированного документа. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag) { get; set; } | Указывает тег, связанный с текущим узлом тега структурированного документа. Не может быть нулевым. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title) { get; set; } | Указывает понятное имя, связанное с этим тегом структурированного документа. Не может быть нулевым. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml) { get; } | Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping) { get; } | Получает объект, представляющий сопоставление этого диапазона тегов структурированного документа с XML data в пользовательской XML-части текущего документа. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild)(Node) | Добавляет указанный узел в конец диапазона stdContent. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанным типам. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| virtual [GetText](../../aspose.words/node/gettext)() | Получает текст этого узла и всех его дочерних элементов. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren)() | Удаляет все узлы между начальным узлом диапазона и конечным узлом диапазона. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly)() | Удаляет это начало диапазона и соответствующие конечные узлы диапазона тега структурированного документа, , но сохраняет его содержимое в дереве документа. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Может быть непосредственным потомком[`Body`](../../aspose.words/body) узел **Только** .

### Примеры

Показывает, как получить свойства тегов структурированного документа, состоящего из нескольких разделов.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Смотрите также

* class [Node](../../aspose.words/node)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
