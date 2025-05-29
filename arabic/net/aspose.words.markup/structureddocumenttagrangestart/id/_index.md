---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTagRangeStart Id—مفتاحك لمعرف رقمي فريد للقراءة فقط لوضع علامات فعالة على المستندات.
type: docs
weight: 40
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

يقوم بتحديد معرف رقمي فريد للقراءة فقط لعلامة المستند المنظم هذه.

```csharp
public int Id { get; }
```

## ملاحظات

يجب أن تتبع سمة المعرف القواعد التالية:

* يجب أن تحتفظ الوثيقة بمعرفات علامات الوثيقة المنظمة فقط إذا تم استنساخ document بالكامل[`Clone`](../../../aspose.words/document/clone/).
* خلال[`ImportNode`](../../../aspose.words/documentbase/importnode/) يجب الاحتفاظ بمعرف إذا لم يتسبب الاستيراد في حدوث تعارضات مع معرفات علامات المستند المنظم الأخرى في المستند المستهدف.
* إذا حددت عدة عقد علامات مستند منظم نفس قيمة الرقم العشري لسمة المعرف، ، فيجب أن تحتفظ علامة المستند المنظم الأولى في المستند بهذا المعرف الأصلي، ويجب أن تحتوي جميع عقد علامات المستند المنظم اللاحقة على معرفات جديدة معينة لها عند تحميل المستند.
* أثناء وضع علامة مستند منظم مستقلINodeCloningListener) سيتم إنشاء معرف فريد جديد للعملية be لعقدة علامة المستند المنظم المستنسخة.
* إذا لم يتم تحديد معرف في المستند المصدر، فيجب أن يكون لعقدة علامة المستند المنظم معرف فريد جديد يتم تعيينه لها عند تحميل المستند.

## أمثلة

يوضح كيفية الحصول على خصائص علامات المستند المنظمة متعددة الأقسام.

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
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
