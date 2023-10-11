---
title: StructuredDocumentTagRangeEnd.Id
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeEnd ملكية. يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لهذا الغرض هيكلةDocumentTagRange العقدة. المقابلةStructuredDocumentTagRangeStart العقدة لديها نفسId .
type: docs
weight: 20
url: /ar/net/aspose.words.markup/structureddocumenttagrangeend/id/
---
## StructuredDocumentTagRangeEnd.Id property

يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لهذا الغرض **هيكلةDocumentTagRange** العقدة. المقابلة[`StructuredDocumentTagRangeStart`](../../structureddocumenttagrangestart/) العقدة لديها نفس[`Id`](../../structureddocumenttagrangestart/id/) .

```csharp
public int Id { get; }
```

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

* class [StructuredDocumentTagRangeEnd](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* المجسم [Aspose.Words](../../../)


