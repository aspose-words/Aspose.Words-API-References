---
title: StructuredDocumentTagRangeStart.Tag
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeStart ملكية. يحدد علامة مرتبطة بعقدة علامة المستند المهيكلة الحالية. لا يمكن أن يكون فارغًا.
type: docs
weight: 150
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/tag/
---
## StructuredDocumentTagRangeStart.Tag property

يحدد علامة مرتبطة بعقدة علامة المستند المهيكلة الحالية. لا يمكن أن يكون فارغًا.

```csharp
public string Tag { get; set; }
```

### ملاحظات

العلامة عبارة عن سلسلة عشوائية يمكن للتطبيقات ربطها بعلامة document المهيكلة من أجل التعرف عليها دون تقديم اسم مألوف مرئي.

### أمثلة

يوضح كيفية الحصول على خصائص علامات المستندات المنظمة متعددة الأقسام.

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

### أنظر أيضا

* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* المجسم [Aspose.Words](../../../)


