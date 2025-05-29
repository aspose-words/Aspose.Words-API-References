---
title: BuildingBlock Class
linktitle: BuildingBlock
articleTitle: BuildingBlock
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.BuildingBlocks.BuildingBlock 类，用于创建和管理词汇表条目（如自动图文集和自动更正），从而提高文档效率。
type: docs
weight: 320
url: /zh/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

代表词汇表文档条目，例如构建基块、自动图文集或自动更正条目。

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class BuildingBlock : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | 指定当构建块的内容插入到主文档时应应用的行为。 |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | 指定构建块的二级分类。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | 获取或设置与此构建块相关的描述。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | 获取构建块中的第一部分。 |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | 指定构建块的第一级分类，以便进行 分类或用户界面排序。 |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | 获取或设置唯一标识此构建块的标识符（128 位 GUID）。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | 获取构建块中的最后一部分。 |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | 获取或设置此构建块的名称。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | 返回BuildingBlock值. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | 返回代表构建块中所有部分的集合。 |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | 指定构建块类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客参观 BuildingBlock 的末尾。 |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客参观 BuildingBlock 的起点。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

`BuildingBlock`仅可包含[`Section`](../../aspose.words/section/)节点。

`BuildingBlock`只能是[`GlossaryDocument`](../glossarydocument/)。

您可以创建新的构建块并将其插入到词汇表文档中。您可以修改或删除现有的构建块。您可以在文档之间复制或移动构建块。您可以将构建块的内容插入到文档中。

对应于**文档部分**，**docPartPr**和**文档部分主体**OOXML 中的元素。

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

* class [CompositeNode](../../aspose.words/compositenode/)
* 命名空间 [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* 部件 [Aspose.Words](../../)
