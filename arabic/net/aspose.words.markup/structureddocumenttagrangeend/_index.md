---
title: StructuredDocumentTagRangeEnd
second_title: Aspose.Words لمراجع .NET API
description: يمثل نهاية تراوحت علامة المستند المهيكلة التي تقبل المحتوى متعدد الأقسام. راجع أيضًاStructuredDocumentTagRangeStart./structureddocumenttagrangestart/ العقدة .
type: docs
weight: 3840
url: /ar/net/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class

يمثل نهاية **تراوحت** علامة المستند المهيكلة التي تقبل المحتوى متعدد الأقسام. راجع أيضًا[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) العقدة .

```csharp
public class StructuredDocumentTagRangeEnd : Node
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [StructuredDocumentTagRangeEnd](structureddocumenttagrangeend/)(DocumentBase, int) | يقوم بتهيئة مثيل جديد لملف **نهاية نطاق علامة المستند المنظم** فئة . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [Id](../../aspose.words.markup/structureddocumenttagrangeend/id/) { get; } | تحديد معرف رقمي فريد ومستمر للقراءة فقط لهذا الغرض **StructuredDocumentTagRange** node. المقابلة[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) العقدة لها نفس الشيء[`Id`](../structureddocumenttagrangestart/id/) . |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangeend/nodetype/) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangeend/accept/)(DocumentVisitor) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

يمكن أن يكون تابعًا فوريًا لـ[`Body`](../../aspose.words/body/) العقدة **فقط** .

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

* class [Node](../../aspose.words/node/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
