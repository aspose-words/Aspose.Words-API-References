---
title: Accept
second_title: Aspose.Words لمراجع .NET API
description: يقبل الزائر .
type: docs
weight: 130
url: /ar/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

يقبل الزائر .

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد ؛ خطأ إذا أوقف برنامج DocumentVisitor العملية قبل زيارة جميع العقد.

### ملاحظات

يعدّ فوق هذه العقدة وجميع توابعها. تستدعي كل عقدة طريقة مقابلة في DocumentVisitor.

لمزيد من المعلومات ، راجع نمط تصميم الزائر.

المكالمات[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) ، ثم يستدعي [`Accept`](../../../aspose.words/node/accept/) لجميع العقد الفرعية لهذه الكتلة البرمجية الإنشائية ، ثم استدعاء [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

ملاحظة: لا تتم زيارة العقدة الإنشائية وتوابعها عند تنفيذ a زائر عبر a[`Document`](../../../aspose.words/document/) إذا كنت ترغب في تنفيذ زائر على كتلة بناء a ، فأنت بحاجة إلى تنفيذ الزائر مرة أخرى[`GlossaryDocument`](../../glossarydocument/) or call`Accept` .

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../buildingblock/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
