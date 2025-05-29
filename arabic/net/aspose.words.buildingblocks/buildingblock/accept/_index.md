---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Accept من BuildingBlock لجذب الزوار بسلاسة وتحسين تجربة المستخدم. أطلق العنان لإمكانات موقعك الإلكتروني اليوم!
type: docs
weight: 130
url: /ar/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

يقبل زائرًا.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيقوم بزيارة العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ خطأ إذا[`DocumentVisitor`](../../../aspose.words/documentvisitor/) تم إيقاف العملية قبل زيارة كافة العقد.

## ملاحظات

يُحصي هذه العقدة وجميع أبنائها. تستدعي كل عقدة طريقة مقابلة على[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات راجع نمط تصميم الزائر.

المكالمات[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) ، ثم يستدعي [`Accept`](../../../aspose.words/node/accept/) لجميع العقد الفرعية لكتلة البناء هذه، ثم قم باستدعاء [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

ملاحظة: لا تتم زيارة عقدة كتلة البناء وأبنائها عندما تقوم بتنفيذ a زائر على[`Document`](../../../aspose.words/document/) إذا كنت تريد تنفيذ زائر عبر كتلة بناء a ، فأنت بحاجة إلى تنفيذ الزائر عبر[`GlossaryDocument`](../../glossarydocument/) or استدعاء`Accept` .

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* المجسم [Aspose.Words](../../../)
