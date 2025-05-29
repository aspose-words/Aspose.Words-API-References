---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: 探索 BuildingBlock 的“接受”方法，无缝衔接访客，提升用户体验。立即释放您网站的全部潜力！
type: docs
weight: 130
url: /zh/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；如果访问了所有节点，则为 false[`DocumentVisitor`](../../../aspose.words/documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举此节点及其所有子节点。每个节点都会调用相应的方法[`DocumentVisitor`](../../../aspose.words/documentvisitor/)。

欲了解更多信息，请参阅访客设计模式。

呼叫[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) ，然后调用 [`Accept`](../../../aspose.words/node/accept/)对于此构建块的所有子节点，然后调用 [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/)。

注意：在执行 a Visitor 时，不会访问构建块节点及其子节点[`Document`](../../../aspose.words/document/)。如果您想对 a 构建块执行访问者，则需要对[`GlossaryDocument`](../../glossarydocument/)or 呼叫`Accept`.

## 例子

展示如何向文档添加自定义构建块。

```csharp
public void CreateAndInsert()
{
    // 文档的词汇表文档存储构建块。
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // 创建一个构建块，命名它，然后将其添加到词汇表文档中。
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // 所有新的构建块 GUID 默认具有相同的零值，我们可以赋予它们一个新的唯一值。
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // 以下属性对构建块进行分类
    // 在菜单中，我们可以通过 Microsoft Word 中的“插入”->“快速部件”->“构建块管理器”进行访问。
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // 在我们将这个构建块添加到我们的文档之前，我们需要给它一些内容，
    // 我们将使用文档访问者来实现。此访问者还将设置类别、图库和行为。
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // 访问 BuildingBlock 的开始/结束。
    block.Accept(visitor);

    // 我们可以从词汇表文档中访问刚刚创建的块。
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // 块本身是包含文本的部分。
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // 现在，我们可以将其作为新部分插入到文档中。
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // 我们也可以在 Microsoft Word 的 Building Blocks Organizer 中找到它并手动放置它。
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// 设置已访问的构建块作为快速部分插入到文档中，并将文本添加到其内容中。
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
        // 将构建块配置为快速部件，并添加构建块管理器使用的属性。
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // 添加带有文本的部分。
        // 将该块插入文档将把该部分及其子节点附加到该位置。
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

### 也可以看看

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* 命名空间 [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* 部件 [Aspose.Words](../../../)
