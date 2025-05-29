---
title: BuildingBlock.Description
linktitle: Description
articleTitle: Description
second_title: Aspose.Words لـ .NET
description: أدر وصف BuildingBlock الخاص بك بسهولة. حدّد أو حدّث الأوصاف بسهولة لتحسين التنظيم والوضوح في مشاريعك.
type: docs
weight: 40
url: /ar/net/aspose.words.buildingblocks/buildingblock/description/
---
## BuildingBlock.Description property

يحصل على الوصف المرتبط بكتلة البناء هذه أو يعينه.

```csharp
public string Description { get; set; }
```

## ملاحظات

قد يحتوي الوصف على أي محتوى سلسلة، وعادةً ما تكون معلومات إضافية.

لا يمكن أن يكون`باطل`، ولكن يمكن أن تكون سلسلة فارغة.

يتوافق مع**وصف docPartPr.** عنصر في OOXML.

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

* class [BuildingBlock](../)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* المجسم [Aspose.Words](../../../)
