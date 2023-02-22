---
title: GlossaryDocument.GetBuildingBlock
second_title: Aspose.Words لمراجع .NET API
description: GlossaryDocument طريقة. البحث عن كتلة إنشاء باستخدام المعرض والفئة والاسم المحدد.
type: docs
weight: 70
url: /ar/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

البحث عن كتلة إنشاء باستخدام المعرض والفئة والاسم المحدد.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| gallery | BuildingBlockGallery | معايير المعرض. |
| category | String | معايير الفئة. يمكن أن يكون فارغًا ، وفي هذه الحالة لن يتم استخدامه للمقارنة. |
| name | String | معايير اسم الكتلة البرمجية الإنشائية. |

### قيمة الإرجاع

الكتلة البرمجية الإنشائية المطابقة أو فارغة إذا لم يتم العثور على تطابق.

### ملاحظات

هذه طريقة ملائمة تتكرر عبر جميع كتل الإنشاء في هذه المجموعة وتُرجع أول كتلة إنشاء تتطابق مع المعرض والفئة والاسم المحدد.

ينظم Microsoft Word اللبنات الأساسية في صالات العرض. تم تعريف galleries مسبقًا باستخدام امتداد[`BuildingBlockGallery`](../../buildingblockgallery/) enum. داخل كل معرض ، يمكن تنظيم الكتل البرمجية الإنشائية في فئة واحدة أو أكثر. اسم الفئة عبارة عن سلسلة. كل كتلة بناء لها اسم. لا يمكن ضمان أن يكون اسم block فريدًا.

### أمثلة

يعرض طرق الوصول إلى الكتل البرمجية الإنشائية في مستند مسرد.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // هناك طرق مختلفة للوصول إلى اللبنات الأساسية.
    // 1 - احصل على اللبنات الأساسية الأولى / الأخيرة في المجموعة:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - احصل على قالب بناء حسب الفهرس:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - احصل على أول قالب إنشائي يطابق معرضًا واسمًا وفئة:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // سنفعل ذلك باستخدام زائر مخصص ،
    // الذي سيعطي كل BuildingBlock في GlossaryDocument GUID فريدًا
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // في Microsoft Word ، يمكننا الوصول إلى اللبنات الأساسية عبر "إدراج" - > "أجزاء سريعة" - >. "منظم كتل البناء".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// يعطي كل كتلة إنشائية في مستند قاموس المصطلحات الذي تمت زيارته GUID فريدًا.
/// يخزن أزواج الكتل البرمجية الإنشائية GUID في قاموس.
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
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../glossarydocument/)
* المجسم [Aspose.Words](../../../)


