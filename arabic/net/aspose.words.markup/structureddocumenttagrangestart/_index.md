---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Markup.StructuredDocumentTagRangeStart، التي تتيح إدارة محتوى متعدد الأقسام بسلاسة في المستندات المنظمة.
type: docs
weight: 4780
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

يمثل بداية**متباعد** علامة مستند منظمة تقبل محتوى متعدد الأقسام. انظر أيضًا[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | يقوم بتهيئة مثيل جديد لـ**بداية نطاق علامة المستند المنظم** الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | يحصل على مظهر علامة المستند المنظم أو يعينه. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | يحصل على لون علامة المستند المنظم أو يعينه. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | يقوم بتحديد معرف رقمي فريد للقراءة فقط لعلامة المستند المنظم هذه. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | يحدد ما إذا كان سيتم تفسير محتوى علامة المستند المنظم هذا بحيث يحتوي على نص نائب (على عكس محتويات النص العادي داخل علامة المستند المنظم). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | يحصل على آخر طفل في نطاق stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | يحصل على المستوى الذي يبدأ عنده نطاق علامة المستند المنظم هذا في شجرة المستند. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | عند ضبطه على`حقيقي` ، ستمنع هذه الخاصية المستخدم من حذف علامة المستند المنظم هذه. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | عند ضبطه على`حقيقي` ، ستمنع هذه الخاصية المستخدم من تحرير محتويات علامة المستند المنظم هذه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | إرجاعStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | يحصل على[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)يحتوي على نص نائب يجب عرضه عندما تكون محتويات علامة المستند المنظم هذه فارغة، يكون عنصر XML المرتبط فارغًا كما هو محدد بواسطة عبر[`XmlMapping`](./xmlmapping/) العنصر أو[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) العنصر هو`حقيقي` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | يحصل على اسم أو تعيينه[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) يحتوي على نص نائب. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | يحدد نهاية النطاق إذا كان[`StructuredDocumentTag`](../structureddocumenttag/) هي علامة مستند منظمة ومحددة النطاق. وإلا فإنها ترجع`باطل` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | يحصل على نوع علامة المستند المنظم هذا. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | يحدد علامة مرتبطة بعقدة علامة المستند المنظم الحالية. لا يمكن`باطل` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | يحدد الاسم الودود المرتبط بعلامة المستند المنظمة هذه. لا يمكن`باطل` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc تنسيق. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc format. على عكس[`WordOpenXML`](./wordopenxml/) الخاصية، هذه الطريقة تولد مستندًا مبسطًا يستبعد أي أجزاء غير مرتبطة بالمحتوى. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | يحصل على كائن يمثل تعيين نطاق علامة المستند المنظم هذا إلى XML data في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | يضيف العقدة المحددة إلى نهاية نطاق stdContent. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق الأنواع المحددة. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| virtual [GetText](../../aspose.words/node/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | يزيل جميع العقد بين عقدة بداية النطاق وعقدة نهاية النطاق. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | يزيل عقدة بداية هذا النطاق وعقدة نهاية النطاق المناسبة لعلامة المستند المنظم، ولكنه يحتفظ بمحتواه داخل شجرة المستند. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

يمكن أن يكون طفلًا مباشرًا لـ[`Body`](../../aspose.words/body/) العقدة**فقط** .

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

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
