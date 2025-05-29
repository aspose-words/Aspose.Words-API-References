---
title: Document.GlossaryDocument
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة مسرد مستنداتك بفعالية. تعلم كيفية تعيين واسترجاع مدخلات المسرد للنص التلقائي وعناصر البناء في قوالبك.
type: docs
weight: 180
url: /ar/net/aspose.words/document/glossarydocument/
---
## Document.GlossaryDocument property

يحصل على أو يعيّن مستند المصطلحات داخل هذا المستند أو القالب. مستند المصطلحات هو مخزن لإدخالات النص التلقائي والتصحيح التلقائي وكتل البناء المحددة في مستند.

```csharp
public GlossaryDocument GlossaryDocument { get; set; }
```

## ملاحظات

هذه الخاصية تعود`باطل` إذا لم يكن للمستند مستند مسرد.

يمكنك إضافة مستند مسرد إلى مستند عن طريق إنشاء a [`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) الكائن وتعيينه لهذه الخاصية.

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

* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
