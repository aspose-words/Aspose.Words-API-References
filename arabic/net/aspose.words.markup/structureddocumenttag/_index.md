---
title: StructuredDocumentTag
second_title: Aspose.Words لمراجع .NET API
description: يمثل علامة مستند منظم SDT أو عنصر تحكم في المحتوى في مستند.
type: docs
weight: 3820
url: /ar/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

يمثل علامة مستند منظم (SDT أو عنصر تحكم في المحتوى) في مستند.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag)(DocumentBase, SdtType, MarkupLevel) | يقوم بتهيئة مثيل جديد لملف **علامة وثيقة منظم** فئة ._ x000d_ |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance) { get; set; } | يحصل / يحدد مظهر علامة مستند منظم. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory) { get; set; } | تحديد فئة الكتلة البرمجية الإنشائية لهذا الغرض **المعاملة الخاصة والتفضيلية** node. لا يمكن أن تكون فارغة . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery) { get; set; } | تحديد نوع الكتلة البرمجية الإنشائية لهذا الغرض **المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون فارغًا . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype) { get; set; } | تحديد نوع التقويم لهذا **المعاملة الخاصة والتفضيلية** . الافتراضي هوDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked) { get; set; } | يحصل / يحدد الحالة الحالية لمربع الاختيار **المعاملة الخاصة والتفضيلية** . القيمة الافتراضية لهذه الخاصية خاطئة. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Color](../../aspose.words.markup/structureddocumenttag/color) { get; set; } | الحصول على أو تحديد لون علامة المستند المهيكلة. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont) { get; } | تنسيق الخط الذي سيتم تطبيقه على النص الذي تم إدخاله فيه **المعاملة الخاصة والتفضيلية** . |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat) { get; set; } | السلسلة التي تمثل التنسيق الذي يتم عرض التواريخ به ._ x000d_ لا يمكن أن تكون خالية ._ x000d_تواريخ اللغة الإنجليزية (الولايات المتحدة) هي "mm / dd / yyyy" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale) { get; set; } | يسمح بتعيين / الحصول على تنسيق اللغة للتاريخ المعروض في هذا **المعاملة الخاصة والتفضيلية** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat) { get; set; } | الحصول على / مجموعات التنسيق الذي يتم فيه تخزين تاريخ تاريخ SDT عندما يكون ملف **المعاملة الخاصة والتفضيلية** مرتبط بعقدة XML في مخزن بيانات المستند. القيمة الافتراضية هيDateTime |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont) { get; } | تنسيق الخط الذي سيتم تطبيقه على الحرف الأخير من النص الذي تم إدخاله فيه **المعاملة الخاصة والتفضيلية** . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate) { get; set; } | يحدد التاريخ الكامل والوقت الذي تم إدخاله مؤخرًا في هذا **المعاملة الخاصة والتفضيلية** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| [Id](../../aspose.words.markup/structureddocumenttag/id) { get; } | يحدد معرّفًا رقميًا فريدًا ومستمرًا للقراءة فقط لهذا الغرض **المعاملة الخاصة والتفضيلية**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext) { get; set; } | يحدد ما إذا كان محتوى هذا **المعاملة الخاصة والتفضيلية** يجب أن يتم تفسيره على أنه يحتوي على عنصر نائب text (على عكس محتويات النص العادي داخل SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary) { get; set; } | يحدد ما إذا كان هذا **المعاملة الخاصة والتفضيلية** يجب إزالتها من مستند WordProcessingML عندما يتم تعديل محتوياته_ x000d_. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [Level](../../aspose.words.markup/structureddocumenttag/level) { get; } | يحصل على المستوى الذي عنده هذا **المعاملة الخاصة والتفضيلية** يحدث في شجرة الوثيقة. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems) { get; } | يحصل[`SdtListItemCollection`](../sdtlistitemcollection) المرتبطة بهذا **المعاملة الخاصة والتفضيلية** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol) { get; set; } | عند التعيين على "صواب" ، ستمنع هذه الخاصية المستخدم من حذف ذلك **المعاملة الخاصة والتفضيلية** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents) { get; set; } | عند التعيين على "صواب" ، ستمنع هذه الخاصية المستخدم من تحرير محتويات هذا **المعاملة الخاصة والتفضيلية** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline) { get; set; } | يحدد ما إذا كان هذا **المعاملة الخاصة والتفضيلية** يسمح بسطر متعددة من النص. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype) { get; } | عوائد **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder) { get; } | يحصل على ملف[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) يحتوي على نص عنصر نائب يجب عرضه عندما تكون محتويات تشغيل SDT فارغة ، يكون عنصر XML المعين المرتبط فارغًا كما هو محدد عبر[`XmlMapping`](./xmlmapping) element أو ملف[`IsShowingPlaceholderText`](./isshowingplaceholdertext) العنصر صحيح. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername) { get; set; } | يحصل أو يحدد اسم[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) تحتوي على نص عنصر نائب. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype) { get; } | يحصل على نوع من هذا **علامة وثيقة منظم** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style) { get; set; } | الحصول على أو تحديد نمط علامة المستند المهيكلة. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename) { get; set; } | الحصول على أو تحديد اسم النمط المطبق على علامة المستند المهيكلة. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag) { get; set; } | يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن يكون فارغًا ._ x000d_ |
| [Title](../../aspose.words.markup/structureddocumenttag/title) { get; set; } | تحديد الاسم المألوف المرتبط بهذا **المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون فارغًا ._ x000d_ |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق ._ x000d_ |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping) { get; } | الحصول على كائن يمثل تعيين علامة المستند المهيكلة هذه إلى بيانات XML في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear)() | يمسح محتويات علامة المستند المهيكلة هذه ويعرض عنصرًا نائبًا إذا تم تحديده. |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة ._ x000d_ |
| override [GetText](../../aspose.words/compositenode/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly)() | يزيل فقط عقدة SDT نفسها ، ولكن يحتفظ بمحتواها داخل شجرة المستند. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | يزيل الكل[`SmartTag`](../smarttag) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol)(int, string) | يعين الرمز المستخدم لتمثيل الحالة المحددة لعنصر تحكم محتوى خانة الاختيار. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol)(int, string) | يعين الرمز المستخدم لتمثيل الحالة غير المحددة لعنصر تحكم محتوى خانة الاختيار. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

تسمح علامات المستندات المنظمة (SDTs) بتضمين دلالات محددة من قبل العميل بالإضافة إلى سلوكها ومظهرها في المستند.

في هذا الإصدار يوفر Aspose.Words عددًا من الأساليب والخصائص العامة لـ للتلاعب بسلوك ومحتوى[`StructuredDocumentTag`](../structureddocumenttag) . يمكن إجراء تعيين عقد SDT لحزم XML المخصصة داخل مستند باستخدام [`XmlMapping`](./xmlmapping) منشأه.

[`StructuredDocumentTag`](../structureddocumenttag) يمكن أن تحدث في مستند في الأماكن التالية:

* مستوى الكتلة - بين الفقرات والجداول ، كطفل من أ[`Body`](../../aspose.words/body) و[`HeaderFooter`](../../aspose.words/headerfooter) ، [`Comment`](../../aspose.words/comment) و[`Footnote`](../../aspose.words.notes/footnote) أو أ[`Shape`](../../aspose.words.drawing/shape) العقدة.
* على مستوى الصفوف - بين الصفوف في الجدول ، كطفل لـ[`Table`](../../aspose.words.tables/table) العقدة.
* على مستوى الخلية - بين الخلايا في صف الجدول ، كطفل في ملف[`Row`](../../aspose.words.tables/row) العقدة.
* المستوى المضمن - من بين المحتوى المضمّن بالداخل ، بصفتك طفلًا في ملف[`Paragraph`](../../aspose.words/paragraph).
* متداخلة داخل أخرى[`StructuredDocumentTag`](../structureddocumenttag).

### أمثلة

يوضح كيفية العمل باستخدام أنماط عناصر التحكم في المحتوى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند إلى علامة مستند منظم.
// 1 - تطبيق كائن نمط من مجموعة أنماط المستند:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - الإشارة إلى نمط في المستند بالاسم:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
