---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: 用于 .NET 的 Aspose.Words
description: GlossaryDocument GetBuildingBlock 方法. 使用指定的图库类别和名称查找构建块 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

使用指定的图库、类别和名称查找构建块。

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| gallery | BuildingBlockGallery | 画廊标准。 |
| category | String | 类别标准。可`无效的`，在这种情况下将不会用于比较。 |
| name | String | 构建块名称标准。 |

### 返回值

匹配的构建块或`无效的`如果没有找到匹配项。

## 评论

这是一种便捷方法，可迭代此集合中的所有构建块 ，并返回与 指定图库、类别和名称匹配的第一个构建块。

Microsoft Word 将构建块组织到库中。 gallery 是使用预定义的[`BuildingBlockGallery`](../../buildingblockgallery/)enum. 在每个库中，构建块可以组织为一个或多个类别。 类别名称是一个字符串。每个构建块都有一个名称。不保证构建块 名称是唯一的。

## 例子

显示访问术语表文档中的构建块的方法。

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

    // 访问构建块的方式有多种。
    // 1 - 获取集合中的第一个/最后一个构建块：
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - 通过索引获取构建块：
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - 获取与画廊、名称和类别匹配的第一个构建块：
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // 我们将使用自定义访问者来做到这一点，
    // 这将为 GlossaryDocument 中的每个 BuildingBlock 提供唯一的 GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);
    Console.WriteLine(visitor.GetText());

    // 在 Microsoft Word 中，我们可以通过“插入”-> 来访问构建块“快速零件”-> “积木组织者”。
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// 为访问的术语表文档中的每个构建块提供唯一的 GUID。
/// 将 GUID 构建块对存储在字典中。
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

### 也可以看看

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* 命名空间 [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* 部件 [Aspose.Words](../../../)
