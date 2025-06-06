---
title: BuildingBlock.Description
linktitle: Description
articleTitle: Description
second_title: Aspose.Words for .NET
description: 轻松管理您的 BuildingBlock 描述。轻松设置或更新描述，增强项目的条理性和清晰度。
type: docs
weight: 40
url: /zh/net/aspose.words.buildingblocks/buildingblock/description/
---
## BuildingBlock.Description property

获取或设置与此构建块相关的描述。

```csharp
public string Description { get; set; }
```

## 评论

描述可以包含任何字符串内容，通常是附加信息。

不可能`无效的`，但可以是空字符串。

对应于**docPartPr.描述** OOXML 中的元素。

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

* class [BuildingBlock](../)
* 命名空间 [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* 部件 [Aspose.Words](../../../)
