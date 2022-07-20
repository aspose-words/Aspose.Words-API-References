---
title: BuildingBlockGallery
second_title: Aspose.Words لمراجع .NET API
description: يحدد المعرض المعرف مسبقًا الذي تم تصنيف الكتلة البرمجية الإنشائية فيه.
type: docs
weight: 150
url: /ar/net/aspose.words.buildingblocks/buildingblockgallery/
---
## BuildingBlockGallery enumeration

يحدد المعرض المعرف مسبقًا الذي تم تصنيف الكتلة البرمجية الإنشائية فيه.

```csharp
public enum BuildingBlockGallery
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| All | `0` | يحدد أن إدخال مستند المسرد هذا يجب أن يقترن بجميع قيم تصنيف المعرض الممكنة. |
| AutoText | `1` |  |
| Bibliography | `2` |  |
| CoverPage | `3` |  |
| CustomAutoText | `4` |  |
| CustomBibliography | `5` |  |
| CustomCoverPage | `6` |  |
| CustomEquations | `7` |  |
| CustomFooters | `8` |  |
| CustomHeaders | `9` |  |
| Custom1 | `10` |  |
| Custom2 | `11` |  |
| Custom3 | `12` |  |
| Custom4 | `13` |  |
| Custom5 | `14` |  |
| CustomPageNumber | `15` |  |
| CustomPageNumberAtBottom | `16` |  |
| CustomPageNumberAtMargin | `17` |  |
| CustomPageNumberAtTop | `18` |  |
| CustomQuickParts | `19` |  |
| CustomTableOfContents | `20` |  |
| CustomTables | `21` |  |
| CustomTextBox | `22` |  |
| CustomWatermarks | `23` |  |
| NoGallery | `24` |  |
| QuickParts | `25` |  |
| Equations | `26` |  |
| Footers | `27` |  |
| Headers | `28` |  |
| PageNumber | `29` |  |
| PageNumberAtBottom | `30` |  |
| PageNumberAtMargin | `31` |  |
| PageNumberAtTop | `32` |  |
| StructuredDocumentTagPlaceholderText | `33` |  |
| TableOfContents | `34` |  |
| Tables | `35` |  |
| TextBox | `36` |  |
| Watermarks | `37` |  |
| Default | `0` | نفسAll . |

### ملاحظات

يتوافق مع **معرض ST_DocPartGallery** اكتب OOXML.

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

* مساحة الاسم [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
