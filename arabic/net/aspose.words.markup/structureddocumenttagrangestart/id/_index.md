---
title: StructuredDocumentTagRangeStart.Id
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeStart ملكية. يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لعلامة المستند المنظمة هذه.
type: docs
weight: 40
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لعلامة المستند المنظمة هذه.

```csharp
public int Id { get; }
```

### ملاحظات

يجب أن تتبع سمة المعرف هذه القواعد:

* يجب أن يحتفظ المستند بمعرفات علامات المستند المنظمة فقط في حالة استنساخ document بأكمله[`Clone`](../../../aspose.words/document/clone/).
* خلال[`ImportNode`](../../../aspose.words/documentbase/importnode/) يجب الاحتفاظ بالمعرف إذا لم يتسبب الاستيراد في حدوث تعارضات مع معرفات علامات المستند المنظمة الأخرى في المستند المستهدف.
* إذا حددت عقد علامات مستند منظم متعددة نفس قيمة الرقم العشري لسمة المعرف، ، فيجب أن تحتفظ علامة المستند المنظم الأولى في المستند بهذا المعرف الأصلي، ويجب أن تحتوي جميع عقد علامات المستند المنظم اللاحقة على معرفات جديدة مخصصة لها عندما تم تحميل المستند.
* خلال علامة المستند المنظمة المستقلةINodeCloningListener)سيتم إنشاء معرف فريد جديد للعملية لعقدة علامة المستند المنظمة المستنسخة.
* إذا لم يتم تحديد المعرف في المستند المصدر، فيجب أن يكون لعقدة علامة المستند المنظمة معرف فريد جديد معين لها عند تحميل المستند.

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


