---
title: StructuredDocumentTagRangeStart.RangeEnd
linktitle: RangeEnd
articleTitle: RangeEnd
second_title: Aspose.Words для .NET
description: Изучите свойства StructuredDocumentTagRangeStart и RangeEnd, чтобы определить границы тегов документа и улучшить структурированное управление документами.
type: docs
weight: 130
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/rangeend/
---
## StructuredDocumentTagRangeStart.RangeEnd property

Указывает конец диапазона, если[`StructuredDocumentTag`](../../structureddocumenttag/) является тегом структурированного документа с диапазоном. В противном случае возвращает`нулевой` .

```csharp
public StructuredDocumentTagRangeEnd RangeEnd { get; }
```

## Примеры

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

* class [StructuredDocumentTagRangeEnd](../../structureddocumenttagrangeend/)
* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
