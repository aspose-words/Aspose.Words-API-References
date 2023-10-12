---
title: StructuredDocumentTagRangeStart.PlaceholderName
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTagRangeStart свойство. Получает или задает ИмяBuildingBlock содержащий текстзаполнитель.
type: docs
weight: 120
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/placeholdername/
---
## StructuredDocumentTagRangeStart.PlaceholderName property

Получает или задает Имя[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель.

[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) с этим именем[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) должен присутствовать в[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) иначеInvalidOperationException произойдет.

```csharp
public string PlaceholderName { get; set; }
```

### Примеры

Показывает, как получить свойства тегов многосекционного структурированного документа.

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

* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* сборка [Aspose.Words](../../../)


