---
title: Class BuildingBlock
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.BuildingBlocks.BuildingBlock فصل. يمثل إدخال مستند المعجم مثل Building Block أو النص التلقائي أو إدخال التصحيح التلقائي.
type: docs
weight: 130
url: /ar/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

يمثل إدخال مستند المعجم مثل Building Block أو النص التلقائي أو إدخال التصحيح التلقائي.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class BuildingBlock : CompositeNode
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [BuildingBlock](buildingblock/)(GlossaryDocument) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | يحدد السلوك الذي يجب تطبيقه عند إدراج محتويات الكتلة البرمجية الإنشائية في المستند الرئيسي. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | يحدد تصنيف المستوى الثاني للكتلة البرمجية الإنشائية. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | الحصول على الوصف المرتبط بالكتلة البرمجية الإنشائية هذه أو تعيينه. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | الحصول على القسم الأول في الكتلة البرمجية الإنشائية. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | يحدد تصنيف المستوى الأول للكتلة البرمجية الإنشائية لأغراض تصنيف أو فرز واجهة المستخدم. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | الحصول على معرف أو تعيينه (معرف GUID 128 بت) الذي يعرّف الكتلة البرمجية الإنشائية هذه بشكل فريد. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | الحصول على القسم الأخير في الكتلة البرمجية الإنشائية. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | الحصول على اسم الكتلة البرمجية الإنشائية هذه أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | إرجاعBuildingBlock القيمة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | إرجاع مجموعة تمثل كافة الأقسام الموجودة في الكتلة البرمجية الإنشائية. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | يحدد نوع الكتلة البرمجية الإنشائية. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(DocumentVisitor) | يقبل الزائر. |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد الأول[`Node`](../../aspose.words/node/) الذي يطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

`BuildingBlock` يمكن أن تحتوي فقط[`Section`](../../aspose.words/section/) العقد.

`BuildingBlock` لا يمكن إلا أن يكون طفلا[`GlossaryDocument`](../glossarydocument/).

يمكنك إنشاء كتل إنشاء جديدة وإدراجها في مستند المسرد. يمكنك تعديل الكتل البرمجية الإنشائية الموجودة أو حذفها. يمكنك نسخ أو نقل كتل الإنشاء بين المستندات. يمكنك إدراج محتوى الكتلة البرمجية الإنشائية في المستند.

يتوافق مع **docPart** , **docPartPr** و **docPartBody** العناصر في OOXML

### أمثلة

يوضح كيفية إضافة كتلة إنشاء مخصصة إلى مستند.

```csharp
public void CreateAndInsert()
{
    // يقوم مستند قاموس المصطلحات الخاص بالمستند بتخزين الكتل البرمجية الإنشائية.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // قم بإنشاء كتلة إنشاء، وقم بتسميتها، ثم قم بإضافتها إلى مستند المسرد.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // جميع المعرفات الفريدة العمومية (GUIDs) الجديدة لها نفس القيمة الصفرية افتراضيًا، ويمكننا منحها قيمة فريدة جديدة.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // الخصائص التالية تصنف الكتل البرمجية الإنشائية
    // في القائمة التي يمكننا الوصول إليها في Microsoft Word عبر "إدراج" -> "الأجزاء السريعة" -> “منظم لبنات البناء”.
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // قبل أن نتمكن من إضافة هذه الكتلة البرمجية الإنشائية إلى مستندنا، سنحتاج إلى إعطائها بعض المحتويات،
    // وهو ما سنفعله باستخدام زائر المستند. سيقوم هذا الزائر أيضًا بتعيين فئة ومعرض وسلوك.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // يمكننا الوصول إلى الكتلة التي أنشأناها للتو من مستند المسرد.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // الكتلة نفسها عبارة عن قسم يحتوي على النص.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // الآن يمكننا إدراجه في المستند كقسم جديد.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // يمكننا أيضًا العثور عليه في Building Blocks Organizer الخاص بـ Microsoft Word ووضعه يدويًا.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// إعداد الكتلة البرمجية الإنشائية التي تمت زيارتها لإدراجها في المستند كجزء سريع وإضافة نص إلى محتوياتها.
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
        // قم بتكوين الكتلة البرمجية الإنشائية كجزء سريع، وأضف الخصائص المستخدمة بواسطة Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // أضف قسمًا يحتوي على نص.
        // سيؤدي إدراج الكتلة في المستند إلى إلحاق هذا القسم بعقده الفرعية في الموقع.
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


