---
title: GlossaryDocument.BuildingBlocks
second_title: Aspose.Words لمراجع .NET API
description: GlossaryDocument ملكية. إرجاع مجموعة مكتوبة تمثل كافة العناصر الأساسية في مستند المسرد.
type: docs
weight: 20
url: /ar/net/aspose.words.buildingblocks/glossarydocument/buildingblocks/
---
## GlossaryDocument.BuildingBlocks property

إرجاع مجموعة مكتوبة تمثل كافة العناصر الأساسية في مستند المسرد.

```csharp
public BuildingBlockCollection BuildingBlocks { get; }
```

### أمثلة

يعرض طرق الوصول إلى الكتل البرمجية الإنشائية في مستند المسرد.

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

    // هناك طرق مختلفة للوصول إلى الكتل البرمجية الإنشائية.
    // 1 - احصل على اللبنات الأولى/الأخيرة في المجموعة:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - الحصول على كتلة بناء حسب الفهرس:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - احصل على أول كتلة بناء تطابق المعرض والاسم والفئة:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // سنفعل ذلك باستخدام زائر مخصص،
    // والذي سيمنح كل BuildingBlock في GlossaryDocument معرفًا فريدًا (GUID).
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);
    Console.WriteLine(visitor.GetText());

    // في Microsoft Word، يمكننا الوصول إلى الكتل البرمجية الإنشائية عبر "إدراج" -> "الأجزاء السريعة" -> “منظم لبنات البناء”.
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// يمنح كل كتلة إنشاء في مستند المسرد الذي تمت زيارته معرفًا فريدًا (GUID).
/// يخزن أزواج كتل بناء GUID في القاموس.
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

* class [BuildingBlockCollection](../../buildingblockcollection/)
* class [GlossaryDocument](../)
* مساحة الاسم [Aspose.Words.BuildingBlocks](../../glossarydocument/)
* المجسم [Aspose.Words](../../../)


