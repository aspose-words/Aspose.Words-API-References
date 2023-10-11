---
title: Class StructuredDocumentTagRangeStart
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart فصل. يمثل بداية تراوحت علامة مستند منظمة تقبل محتوى متعدد الأقسام. راجع أيضًاStructuredDocumentTagRangeEnd .
type: docs
weight: 4090
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

يمثل بداية **تراوحت** علامة مستند منظمة تقبل محتوى متعدد الأقسام. راجع أيضًا[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(DocumentBase, SdtType) | تهيئة مثيل جديد لـ **يبدأ نطاق علامات المستند المنظم** فئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | يحصل على كافة العقد بين عقدة بداية النطاق وعقدة نهاية النطاق. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | الحصول على أو تعيين لون علامة المستند المنظمة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لعلامة المستند المنظمة هذه. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | يحدد ما إذا كان يجب تفسير محتوى علامة المستند المنظم هذه بحيث يحتوي على نص نائب (على عكس محتويات النص العادي داخل علامة المستند المنظم). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | الحصول على الطفل الأخير في نطاق stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | الحصول على المستوى الذي يبدأ عنده نطاق علامات المستند الهيكلي هذا في شجرة المستندات. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | عند الضبط على`حقيقي` ، ستمنع هذه الخاصية المستخدم من حذف علامة المستند المنظمة هذه. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | عند الضبط على`حقيقي` ، ستمنع هذه الخاصية المستخدم من تحرير محتويات علامة المستند المنظمة هذه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | إرجاعStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | يحصل على[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)يحتوي على نص عنصر نائب يجب عرضه عندما تكون محتويات تشغيل علامة المستند المنظمة هذه فارغة، وعنصر XML المعين المرتبط فارغ كما هو محدد عبر[`XmlMapping`](./xmlmapping/) العنصر أو[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) العنصر هو`حقيقي` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | الحصول على أو تعيين اسم[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) تحتوي على نص نائب. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | يحدد نهاية النطاق إذا كان[`StructuredDocumentTag`](../structureddocumenttag/) هي علامة مستند منظمة ذات نطاق محدد. وإلا يعود`باطل` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | الحصول على نوع علامة المستند المنظمة هذه. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | يحدد علامة مرتبطة بعقدة علامة المستند المنظمة الحالية. لا يمكن أن يكون`باطل` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | يحدد الاسم المألوف المرتبط بعلامة المستند المنظمة هذه. لا يمكن أن يكون`باطل` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | الحصول على كائن يمثل تعيين نطاق علامات المستند المنظم هذا إلى بيانات XML في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(DocumentVisitor) | يقبل الزائر. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(Node) | إضافة العقدة المحددة إلى نهاية نطاق stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق الأنواع المحددة. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| virtual [GetText](../../aspose.words/node/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | إزالة كافة العقد بين عقدة بداية النطاق وعقدة نهاية النطاق. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | يزيل هذا النطاق بداية وعقد نهاية النطاق المناسبة لعلامة المستند المنظمة، ولكنه يحتفظ بمحتواه داخل شجرة المستند. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

يمكن أن يكون الطفل المباشر لـ[`Body`](../../aspose.words/body/) العقدة **فقط** .

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
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


