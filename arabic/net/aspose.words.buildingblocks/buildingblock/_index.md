---
title: Class BuildingBlock
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.BuildingBlocks.BuildingBlock فصل. يمثل إدخال مستند مسرد مثل Building Block أو AutoText أو إدخال التصحيح التلقائي.
type: docs
weight: 120
url: /ar/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

يمثل إدخال مستند مسرد مثل Building Block أو AutoText أو إدخال التصحيح التلقائي.

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
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | يحدد السلوك الذي يجب تطبيقه عند إدراج محتويات block في المستند الرئيسي. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | يحدد تصنيف المستوى الثاني للكتلة البرمجية الإنشائية. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [Count](../../aspose.words/compositenode/count/) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | الحصول على الوصف المرتبط بهذه الكتلة البرمجية الإنشائية أو تعيينه. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | يحصل على القسم الأول في الكتلة البرمجية الإنشائية . |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | يحدد تصنيف المستوى الأول للكتلة البرمجية الإنشائية لأغراض تصنيف أو فرز واجهة المستخدم . |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | الحصول على أو تعيين معرّف (128 بت GUID) يعرّف بشكل فريد كتلة الإنشاء هذه. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | الحصول على آخر تابع للعقدة . |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | يحصل على القسم الأخير في الكتلة البرمجية الإنشائية . |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | الحصول على اسم الكتلة البرمجية الإنشائية هذه أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | إرجاع ملفBuildingBlock القيمة . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | إرجاع مجموعة تمثل كافة الأقسام في الكتلة البرمجية الإنشائية. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | يحدد نوع الكتلة البرمجية الإنشائية . |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(DocumentVisitor) | يقبل الزائر . |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة . |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد التابعة للعقدة الحالية. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

`BuildingBlock` يمكن أن تحتوي فقط[`Section`](../../aspose.words/section/) العقد.

`BuildingBlock` يمكن أن يكون فقط تابعًا لـ[`GlossaryDocument`](../glossarydocument/).

يمكنك إنشاء كتل إنشاء جديدة وإدراجها في مستند قاموس المصطلحات . يمكنك تعديل أو حذف الكتل البرمجية الإنشائية الموجودة. يمكنك نسخ أو نقل الكتل البرمجية الإنشائية بين المستندات. يمكنك إدراج محتوى الكتلة البرمجية الإنشائية في مستند.

يتوافق مع **docPart** و **docPartPr** و **docPartBody**العناصر في OOXML.

### أمثلة

يوضح كيفية إضافة كتلة إنشاء مخصصة إلى مستند.

```csharp
public void CreateAndInsert()
{
    // مسرد الوثيقة يخزن المستند اللبنات الأساسية.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // قم بإنشاء كتلة إنشاء ، وقم بتسميتها ، ثم قم بإضافتها إلى مستند المسرد.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // كل كتل الإنشاء الجديدة GUIDs لها نفس القيمة الصفرية افتراضيًا ، ويمكننا منحها قيمة فريدة جديدة.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // تصنف الخصائص التالية اللبنات الأساسية
    // في القائمة يمكننا الوصول إليها في Microsoft Word عبر "إدراج" - >; "أجزاء سريعة" - >. "منظم كتل البناء".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // قبل أن نتمكن من إضافة هذه الكتلة البرمجية الإنشائية إلى وثيقتنا ، سنحتاج إلى إعطائها بعض المحتويات ،
    // الذي سنفعله باستخدام زائر المستند. سيقوم هذا الزائر أيضًا بتعيين فئة ومعرض وسلوك.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // يمكننا الوصول إلى الكتلة التي أنشأناها للتو من مستند المسرد.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // الكتلة نفسها هي قسم يحتوي على النص.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // الآن ، يمكننا إدراجه في المستند كقسم جديد.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // يمكننا أيضًا العثور عليه في منظم قوالب البناء الخاص بـ Microsoft Word ووضعه يدويًا.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// يقوم بإعداد كتلة إنشاء تمت زيارتها لإدراجها في المستند كجزء سريع وإضافة نص إلى محتوياتها.
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
        // تكوين الكتلة البرمجية الإنشائية كجزء سريع ، وإضافة الخصائص المستخدمة بواسطة Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // إضافة قسم مع النص.
        // سيؤدي إدراج الكتلة في المستند إلى إلحاق هذا القسم بالعقد الفرعية في الموقع.
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


