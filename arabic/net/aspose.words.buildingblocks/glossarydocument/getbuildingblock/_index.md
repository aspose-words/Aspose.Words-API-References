---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GlossaryDocument GetBuildingBlock لتحديد مواقع كتل البناء بكفاءة حسب فئة المعرض واسمه. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 90
url: /ar/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

يبحث عن كتلة بناء باستخدام المعرض والفئة والاسم المحددين.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| gallery | BuildingBlockGallery | معايير المعرض. |
| category | String | معايير الفئة. يمكن أن تكون`باطل`وفي هذه الحالة لن يتم استخدامه للمقارنة. |
| name | String | معايير اسم كتلة البناء. |

### قيمة الإرجاع

كتلة البناء المطابقة أو`باطل` إذا لم يتم العثور على تطابق.

## ملاحظات

هذه طريقة ملائمة تتكرر على كل كتل البناء في هذه المجموعة وترجع أول كتلة بناء تتطابق مع المعرض والفئة والاسم المحددين.

يُنظّم Microsoft Word كتل البناء في معارض. يتم تعريف galleries مسبقًا باستخدام[`BuildingBlockGallery`](../../buildingblockgallery/)enum. ضمن كل معرض، يمكن تنظيم كتل البناء في فئة واحدة أو أكثر. اسم الفئة عبارة عن سلسلة نصية. لكل كتلة بناء اسم. لا يُضمن أن يكون اسم كتلة البناء فريدًا.

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

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* المجسم [Aspose.Words](../../../)
