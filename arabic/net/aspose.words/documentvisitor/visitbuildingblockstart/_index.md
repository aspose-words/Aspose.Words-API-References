---
title: DocumentVisitor.VisitBuildingBlockStart
linktitle: VisitBuildingBlockStart
articleTitle: VisitBuildingBlockStart
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentVisitor VisitBuildingBlockStart، وهي أساسية لبدء تعداد كتل البناء. حسّن كفاءة ترميزك اليوم!
type: docs
weight: 70
url: /ar/net/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor.VisitBuildingBlockStart method

يتم استدعاؤها عند بدء تعداد كتلة البناء.

```csharp
public virtual VisitorAction VisitBuildingBlockStart(BuildingBlock block)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| block | BuildingBlock | الشيء الذي يتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية مواصلة التعداد.

## ملاحظات

ملاحظة: لا تتم زيارة عقدة كتلة البناء وأبنائها عندما تقوم بتنفيذ a زائر على[`Document`](../../document/) إذا كنت تريد تنفيذ زائر عبر كتلة بناء a ، فأنت بحاجة إلى تنفيذ الزائر عبر[`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) or استدعاء[`Accept`](../../../aspose.words.buildingblocks/buildingblock/accept/) .

## أمثلة

يوضح طرق الوصول إلى كتل البناء في مستند المصطلحات.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // هناك طرق مختلفة للوصول إلى كتل البناء.
    // 1 - احصل على أول/آخر كتلة بناء في المجموعة:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - الحصول على كتلة بناء حسب الفهرس:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - احصل على أول كتلة بناء تتطابق مع المعرض والاسم والفئة:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // سوف نفعل ذلك باستخدام زائر مخصص،
    // مما سيعطي لكل BuildingBlock في GlossaryDocument معرف GUID فريدًا
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // قم بزيارة بداية/نهاية مستند المصطلحات.
    glossaryDoc.Accept(visitor);
    // قم بزيارة بداية مستند المصطلحات فقط.
    glossaryDoc.AcceptStart(visitor);
    // قم بزيارة نهاية مستند المصطلحات فقط.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // في Microsoft Word، يمكننا الوصول إلى كتل البناء عبر "إدراج" -> "الأجزاء السريعة" -> "منظم كتل البناء".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// يمنح كل كتلة بناء في مستند المصطلحات الذي تمت زيارتها معرف GUID فريدًا.
/// يخزن أزواج كتلة بناء GUID في القاموس.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
