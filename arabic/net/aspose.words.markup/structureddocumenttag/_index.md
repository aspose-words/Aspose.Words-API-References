---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Markup.StructuredDocumentTag للتحكم الفعال في محتوى المستندات. حسّن إدارة مستنداتك مع ميزات SDT!
type: docs
weight: 4750
url: /ar/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

يمثل علامة مستند منظمة (SDT أو عنصر تحكم المحتوى) في مستند.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | يقوم بتهيئة مثيل جديد لـ**علامة المستند المنظم** الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | يحصل على/يحدد مظهر علامة المستند المنظمة. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | يحدد فئة كتلة البناء لهذا**SDT** node. لا يمكن`باطل` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | يحدد نوع كتلة البناء لهذا**SDT** . لا يمكن`باطل` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | يحدد نوع التقويم لهذا**SDT** . الافتراضي هوDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | يحصل على/يحدد الحالة الحالية لمربع الاختيار**SDT** . القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | يحصل على لون علامة المستند المنظم أو يعينه. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | تنسيق الخط الذي سيتم تطبيقه على النص المدخل في**SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | سلسلة تمثل التنسيق الذي يتم به عرض التواريخ. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | يسمح بتعيين/الحصول على تنسيق اللغة للتاريخ المعروض في هذا**SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | يحصل/يحدد التنسيق الذي يتم به تخزين التاريخ لتاريخ SDT عندما**SDT** مرتبط بعقدة XML في مخزن بيانات المستند. القيمة الافتراضية هيDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | تنسيق الخط الذي سيتم تطبيقه على آخر حرف من النص المدخل**SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | يحدد التاريخ الكامل والوقت الذي تم إدخاله آخر مرة في هذا**SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | يحدد معرفًا رقميًا فريدًا للقراءة فقط لهذا**SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | يحدد ما إذا كان محتوى هذا**SDT** يجب تفسيره بحيث يحتوي على نص نائب (على عكس محتويات النص العادي داخل SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | يحدد ما إذا كان هذا**SDT** يجب إزالته من مستند WordProcessingML عند تعديل محتوياته . |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | يحصل على المستوى الذي يتم فيه هذا**SDT** يحدث في شجرة المستندات. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | يحصل[`SdtListItemCollection`](../sdtlistitemcollection/) مرتبط بهذا**SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | عند ضبطه على`حقيقي` ، هذه الخاصية سوف تمنع المستخدم من حذف هذا**SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | عند ضبطه على`حقيقي` ، هذه الخاصية سوف تمنع المستخدم من تحرير محتويات هذه**SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | يحدد ما إذا كان هذا**SDT** يسمح بخطوط متعددة من النص. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | إرجاعStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | يحصل على[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) يحتوي على نص نائب يجب عرضه عندما تكون محتويات تشغيل SDT هذه فارغة، يكون عنصر XML المرتبط فارغًا كما هو محدد عبر[`XmlMapping`](./xmlmapping/) element أو[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) العنصر هو`حقيقي` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | يحصل على اسم أو تعيينه[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) يحتوي على نص نائب. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | يحصل على نوع من هذا**علامة المستند المنظم** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | يحصل على نمط علامة المستند المنظم أو يعينه. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | يحصل على اسم النمط المطبق على علامة المستند المنظم أو يعينه. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن`باطل` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | يحدد الاسم الودي المرتبط بهذا**SDT** . لا يمكن`باطل` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc تنسيق. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc format. على عكس[`WordOpenXML`](./wordopenxml/) الخاصية، هذه الطريقة تولد مستندًا مبسطًا يستبعد أي أجزاء غير مرتبطة بالمحتوى. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | يحصل على كائن يمثل تعيين علامة المستند المنظم هذه إلى XML data في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة نهاية StructuredDocumentTag. |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة بداية StructuredDocumentTag. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | يمسح محتويات علامة المستند المنظمة هذه ويعرض عنصرًا نائبًا إذا تم تعريفه. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | يزيل عقدة SDT هذه فقط، لكنه يحتفظ بمحتوياتها داخل شجرة المستندات. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../../aspose.words/node/) الذي يتطابق مع تعبير XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | يحدد الرمز المستخدم لتمثيل حالة تحديد عنصر التحكم في محتوى مربع الاختيار. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | يحدد الرمز المستخدم لتمثيل حالة عدم تحديد عنصر التحكم في محتوى مربع الاختيار. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

تسمح علامات المستندات المنظمة (SDTs) بتضمين الدلالات التي يحددها العميل بالإضافة إلى سلوك its ومظهره في مستند.

في هذا الإصدار، يوفر Aspose.Words عددًا من الطرق والخصائص العامة لـ للتلاعب بسلوك ومحتوى`StructuredDocumentTag` . يمكن إجراء تعيين عقد SDT إلى حزم XML مخصصة داخل مستند باستخدام [`XmlMapping`](./xmlmapping/) ملكية.

`StructuredDocumentTag` يمكن أن يحدث في مستند في الأماكن التالية:

* على مستوى الكتلة - بين الفقرات والجداول، كطفل لـ[`Body`](../../aspose.words/body/) ،[`HeaderFooter`](../../aspose.words/headerfooter/) ، [`Comment`](../../aspose.words/comment/) ،[`Footnote`](../../aspose.words.notes/footnote/) أو أ[`Shape`](../../aspose.words.drawing/shape/) العقدة.
* على مستوى الصف - بين الصفوف في جدول، كطفل لـ[`Table`](../../aspose.words.tables/table/) العقدة.
* على مستوى الخلية - بين الخلايا في صف الجدول، كطفل لـ[`Row`](../../aspose.words.tables/row/) العقدة.
* على المستوى المضمن - من بين المحتوى المضمن بالداخل، باعتباره طفلًا لـ[`Paragraph`](../../aspose.words/paragraph/).
* متداخلة داخل أخرى`StructuredDocumentTag`.

## أمثلة

يوضح كيفية العمل مع الأنماط لعناصر التحكم في المحتوى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند على علامة مستند منظمة.
// 1 - تطبيق كائن نمط من مجموعة أنماط المستند:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - الإشارة إلى النمط في المستند بالاسم:
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
