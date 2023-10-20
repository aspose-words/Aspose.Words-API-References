---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Markup.StructuredDocumentTag فصل. يمثل علامة مستند منظمة SDT أو التحكم في المحتوى في المستند في C#.
type: docs
weight: 4060
url: /ar/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

يمثل علامة مستند منظمة (SDT أو التحكم في المحتوى) في المستند.

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | تهيئة مثيل جديد لـ**علامة الوثيقة المنظمة** فئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | الحصول على/تعيين مظهر علامة المستند المنظمة. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | يحدد فئة الكتلة البرمجية الإنشائية لهذا الغرض**المعاملة الخاصة والتفضيلية** العقدة. لا يمكن أن يكون`باطل` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | يحدد نوع الكتلة البرمجية الإنشائية لهذا الغرض**المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون`باطل` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | يحدد نوع التقويم لذلك**المعاملة الخاصة والتفضيلية** . الافتراضي هوDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | الحصول على/تعيين الحالة الحالية لمربع الاختيار**المعاملة الخاصة والتفضيلية** . القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | الحصول على أو تعيين لون علامة المستند المنظمة. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | تنسيق الخط الذي سيتم تطبيقه على النص الذي تم إدخاله**المعاملة الخاصة والتفضيلية** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | سلسلة تمثل التنسيق الذي يتم عرض التواريخ به. لا يمكن أن يكون`باطل` . التواريخ للغة الإنجليزية (الولايات المتحدة) هي "mm/dd/yyyy" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | يسمح بتعيين/الحصول على تنسيق اللغة للتاريخ المعروض في هذا**المعاملة الخاصة والتفضيلية** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | تنسيق Get/sets الذي يتم فيه تخزين تاريخ SDT عندما**المعاملة الخاصة والتفضيلية**يرتبط بعقدة XML في مخزن بيانات المستند. القيمة الافتراضية هيDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | تنسيق الخط الذي سيتم تطبيقه على الحرف الأخير من النص الذي تم إدخاله**المعاملة الخاصة والتفضيلية** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | يحدد التاريخ والوقت الكاملين لآخر إدخال في هذا**المعاملة الخاصة والتفضيلية** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لهذا الغرض**المعاملة الخاصة والتفضيلية**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | يحدد ما إذا كان محتوى هذا**المعاملة الخاصة والتفضيلية**يجب تفسيره على أنه يحتوي على العنصر النائب text (على عكس محتويات النص العادي ضمن المعاملة الخاصة والتفضيلية). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | يحدد ما إذا كان هذا**المعاملة الخاصة والتفضيلية** ستتم إزالته من مستند WordProcessingML عند تعديل محتوياته . |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | يحصل على المستوى الذي عنده**المعاملة الخاصة والتفضيلية** يحدث في شجرة المستندات. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | يحصل[`SdtListItemCollection`](../sdtlistitemcollection/) المرتبطة بهذا**المعاملة الخاصة والتفضيلية** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | عند الضبط على`حقيقي` ، ستمنع هذه الخاصية المستخدم من حذف هذا**المعاملة الخاصة والتفضيلية** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | عند الضبط على`حقيقي` ، ستمنع هذه الخاصية المستخدم من تحرير محتويات هذا**المعاملة الخاصة والتفضيلية** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | يحدد ما إذا كان هذا**المعاملة الخاصة والتفضيلية** يسمح بعدة أسطر من النص. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | إرجاعStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | يحصل على[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)يحتوي على نص عنصر نائب يجب عرضه عندما تكون محتويات تشغيل SDT فارغة، عنصر XML المعين المرتبط فارغ كما هو محدد عبر[`XmlMapping`](./xmlmapping/) element أو[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) العنصر هو`حقيقي` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | الحصول على أو تعيين اسم[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) تحتوي على نص نائب. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | يحصل على نوع من هذا**علامة الوثيقة المنظمة** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | الحصول على نمط علامة المستند المنظمة أو تعيينه. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | الحصول على أو تعيين اسم النمط المطبق على علامة المستند المنظمة. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن يكون`باطل` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | يحدد الاسم المألوف المرتبط بهذا**المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون`باطل` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc تنسيق. خلافا ل[`WordOpenXML`](./wordopenxml/)الخاصية، تقوم هذه الطريقة بإنشاء مستند مبسط يستبعد أي أجزاء غير متعلقة بالمحتوى. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | الحصول على كائن يمثل تعيين علامة المستند المنظمة هذه إلى بيانات XML في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | إضافة العقدة المحددة إلى نهاية قائمة العقد التابعة لهذه العقدة. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | يمسح محتويات علامة المستند المنظمة ويعرض عنصرًا نائبًا إذا تم تعريفه. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | إضافة العقدة المحددة إلى بداية قائمة العقد التابعة لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | إزالة العقدة الفرعية المحددة. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | إزالة عقدة SDT نفسها فقط، مع الاحتفاظ بمحتواها داخل شجرة المستندات. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | تحديد الأول[`Node`](../../aspose.words/node/) الذي يطابق تعبير XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | يعين الرمز المستخدم لتمثيل الحالة المحددة لعنصر تحكم محتوى خانة الاختيار. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | يعين الرمز المستخدم لتمثيل الحالة غير المحددة لعنصر التحكم في محتوى خانة الاختيار. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

تسمح علامات المستندات المنظمة (SDTs) بتضمين دلالات محددة من قبل العميل بالإضافة إلى سلوكها ومظهرها في المستند.

في هذا الإصدار، يوفر Aspose.Words عددًا من الأساليب والخصائص العامة للتعامل مع سلوك ومحتوى`StructuredDocumentTag` . يمكن إجراء تعيين عقد SDT لحزم XML المخصصة داخل المستند باستخدام [`XmlMapping`](./xmlmapping/) ملكية.

`StructuredDocumentTag` يمكن أن يحدث في مستند في الأماكن التالية:

* مستوى الكتلة - بين الفقرات والجداول، كطفل لـ a[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/)[`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) أو أ[`Shape`](../../aspose.words.drawing/shape/) العقدة.
* مستوى الصف - بين الصفوف في الجدول، كطفل لـ a[`Table`](../../aspose.words.tables/table/) العقدة.
* مستوى الخلية - بين الخلايا الموجودة في صف الجدول، كفرع لـ a[`Row`](../../aspose.words.tables/row/) العقدة.
* المستوى المضمن - من بين المحتوى المضمن بالداخل، كطفل لـ[`Paragraph`](../../aspose.words/paragraph/).
* متداخلة داخل آخر`StructuredDocumentTag`.

## أمثلة

يوضح كيفية العمل مع أنماط عناصر التحكم في المحتوى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند على علامة مستند منظمة.
// 1 - تطبيق كائن نمط من مجموعة أنماط المستند:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - قم بالإشارة إلى النمط الموجود في المستند بالاسم:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
