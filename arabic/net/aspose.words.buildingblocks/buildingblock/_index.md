---
title: BuildingBlock Class
linktitle: BuildingBlock
articleTitle: BuildingBlock
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.BuildingBlocks.BuildingBlock لإنشاء وإدارة إدخالات المصطلحات مثل AutoText وAutoCorrect لتحسين كفاءة المستند.
type: docs
weight: 320
url: /ar/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

يمثل إدخال مستند المصطلحات مثل إدخال كتلة البناء أو النص التلقائي أو التصحيح التلقائي.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class BuildingBlock : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | يحدد السلوك الذي سيتم تطبيقه عند إدراج محتويات كتلة البناء في المستند الرئيسي. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | يحدد تصنيف المستوى الثاني لكتلة البناء. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | يحصل على الوصف المرتبط بكتلة البناء هذه أو يعينه. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | يحصل على القسم الأول في كتلة البناء. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | يحدد تصنيف المستوى الأول لكتلة البناء لأغراض تصنيف أو فرز واجهة المستخدم. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | يحصل على أو يعين معرفًا (GUID مكون من 128 بت) يحدد كتلة البناء هذه بشكل فريد. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | يحصل على القسم الأخير في كتلة البناء. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | يحصل على اسم كتلة البناء هذه أو يعينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | يعيدBuildingBlock القيمة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | يعيد مجموعة تمثل جميع الأقسام في كتلة البناء. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | يحدد نوع كتلة البناء. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة نهاية BuildingBlock. |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا لزيارة بداية BuildingBlock. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../../aspose.words/node/) الذي يتطابق مع تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

`BuildingBlock` يمكن أن تحتوي فقط[`Section`](../../aspose.words/section/) العقد.

`BuildingBlock` لا يمكن أن يكون إلا طفلا[`GlossaryDocument`](../glossarydocument/).

يمكنك إنشاء كتل بناء جديدة وإدراجها في مستند مسرد. يمكنك تعديل أو حذف كتل بناء موجودة. يمكنك نسخ أو نقل كتل البناء بين المستندات. يمكنك أيضًا إدراج محتوى كتلة بناء في مستند.

يتوافق مع**docPart** ،**docPartPr** و**docPartBody**العناصر في OOXML.

## أمثلة

يوضح كيفية إضافة كتلة بناء مخصصة إلى مستند.

```csharp
public void CreateAndInsert()
{
    // تخزن قائمة المصطلحات الخاصة بالمستند عناصر البناء.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // قم بإنشاء كتلة بناء، وقم بتسميتها، ثم أضفها إلى مستند المصطلحات.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // تحتوي جميع معرفات GUID الجديدة الخاصة بكتل البناء على نفس القيمة الصفرية بشكل افتراضي، ويمكننا منحها قيمة فريدة جديدة.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // الخصائص التالية تصنف كتل البناء
    // في القائمة يمكننا الوصول إليها في Microsoft Word عبر "إدراج" -> "الأجزاء السريعة" -> "منظم كتل البناء".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // قبل أن نتمكن من إضافة كتلة البناء هذه إلى مستندنا، سنحتاج إلى إعطائها بعض المحتويات،
    // سنستخدم زائر مستند. سيُحدد هذا الزائر أيضًا فئةً ومعرضًا وسلوكًا.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // قم بزيارة بداية/نهاية BuildingBlock.
    block.Accept(visitor);

    //يمكننا الوصول إلى الكتلة التي أنشأناها للتو من مستند المصطلحات.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // الكتلة نفسها عبارة عن قسم يحتوي على النص.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // الآن، يمكننا إدراجه في المستند كقسم جديد.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // يمكننا أيضًا العثور عليه في Building Blocks Organizer في Microsoft Word ووضعه يدويًا.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// يقوم بإعداد كتلة بناء تمت زيارتها ليتم إدراجها في المستند كجزء سريع ويضيف نصًا إلى محتوياته.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // قم بتكوين كتلة البناء كجزء سريع، وأضف الخصائص التي يستخدمها منظم كتل البناء.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        //أضف قسمًا يحتوي على نص.
        // سيؤدي إدراج الكتلة في المستند إلى إضافة هذا القسم مع العقد الفرعية الخاصة به في الموقع.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### أنظر أيضا

* class [CompositeNode](../../aspose.words/compositenode/)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* المجسم [Aspose.Words](../../)
