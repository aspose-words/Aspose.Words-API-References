---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: Aspose.Words for .NET
description: 探索 GlossaryDocument 的 GetBuildingBlock 方法，按图库类别和名称高效查找构建块。立即提升您的文档管理能力！
type: docs
weight: 90
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
| category | String | 类别标准。可以是`无效的`，在这种情况下它将不会用于比较。 |
| name | String | 构建块名称标准。 |

### 返回值

匹配的构建块或`无效的`如果没有找到匹配项。

## 评论

这是一种便捷方法，它遍历此集合中的所有构建块并返回与指定的图库、类别和名称匹配的第一个构建块。

Microsoft Word 将构建块组织到图库中。galleries 是使用[`BuildingBlockGallery`](../../buildingblockgallery/)枚举。 在每个图库中，构建块可以组织成一个或多个类别。 类别名称是一个字符串。每个构建块都有一个名称。构建块 的名称不保证唯一。

## 例子

展示访问词汇表文档中的构建块的方法。

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

    // 有多种访问构建块的方法。
    // 1 - 获取集合中的第一个/最后一个构建块：
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - 通过索引获取构建块：
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - 获取与画廊、名称和类别匹配的第一个构建块：
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // 我们将使用自定义访问者来实现这一点，
    // 这将为 GlossaryDocument 中的每个 BuildingBlock 提供唯一的 GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // 访问词汇表文档的开始/结束。
    glossaryDoc.Accept(visitor);
    // 仅访问词汇表文档的开头。
    glossaryDoc.AcceptStart(visitor);
    // 仅访问词汇表文档的末尾。
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // 在 Microsoft Word 中，我们可以通过“插入”->“快速部件”->“构建块管理器”访问构建块。
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// 为访问的词汇表文档中的每个构建块提供唯一的 GUID。
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
