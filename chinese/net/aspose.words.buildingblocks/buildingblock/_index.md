---
title: BuildingBlock
second_title: Aspose.Words for .NET API 参考
description: 表示词汇表文档条目例如 Building Block自动图文集或自动更正条目
type: docs
weight: 120
url: /zh/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

表示词汇表文档条目，例如 Building Block、自动图文集或自动更正条目。

```csharp
public class BuildingBlock : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [BuildingBlock](buildingblock)(GlossaryDocument) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior) { get; set; } | 指定将构建块 的内容插入主文档时应应用的行为。 |
| [Category](../../aspose.words.buildingblocks/buildingblock/category) { get; set; } | 指定构建块的二级分类。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| [Description](../../aspose.words.buildingblocks/buildingblock/description) { get; set; } | 获取或设置与此构建块关联的描述。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection) { get; } | 获取构建块中的第一部分。 |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery) { get; set; } | 为 分类或用户界面排序指定构建块的第一级分类。 |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid) { get; set; } | 获取或设置唯一标识此构建块的标识符（128 位 GUID）。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection) { get; } | 获取构建块中的最后一个部分。 |
| [Name](../../aspose.words.buildingblocks/buildingblock/name) { get; set; } | 获取或设置此构建块的名称。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype) { get; } | 返回BuildingBlock值。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections) { get; } | 返回代表构建块中所有部分的集合。 |
| [Type](../../aspose.words.buildingblocks/buildingblock/type) { get; set; } | 指定构建块类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept)(DocumentVisitor) | 接受访问者。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定[`NodeType`](../../aspose.words/nodetype)的第一个祖先。 |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | 为在此节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext)() | 获取该节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | 在指定参考节点之前插入指定节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | 移除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | 删除当前节点的所有[`SmartTag`](../../aspose.words.markup/smarttag)后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

[`BuildingBlock`](../buildingblock)可以包含只有[`Section`](../../aspose.words/section)节点。

[`BuildingBlock`](../buildingblock)只能是GlossaryDocument。

您可以创建新的构建块并将它们插入到词汇表文档中。 您可以修改或删除现有的构建块。您可以在文档之间复制或移动构建基块 。您可以将构建块的内容插入到文档中。

对应于 **docPart** , **docPartPr** 和 **docPartBody**OOXML 中的元素。

### 例子

显示如何将自定义构建块添加到一个文件。

```csharp
public void CreateAndInsert()
{
     // 文档的词汇表文档存储构建块.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

     // 创建一个积木，命名，然后将其添加到词汇表文档中。
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

     // 所有新的构建块 GUID 默认都具有相同的零值，我们可以给它们一个新的唯一值。
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

     // 以下属性对构建块进行分类
     // 在菜单中，我们可以通过“插入”在 Microsoft Word 中访问 -> “快速零件”-> “积木组织者”.
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

     // 在我们可以将这个构建块添加到我们的文档之前，我们需要给它一些内容，
     // 我们将使用文档访问者来完成。此访问者还将设置类别、画廊和行为。
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // 我们可以访问我们刚刚从词汇表文档中创建的块。
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

     // 块本身是一个包含文本的部分。
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

     // 现在，我们可以将它作为一个新部分插入到文档中。
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

     // 我们也可以在 Microsoft Word 的 Building Blocks Organizer 中找到并手动放置。
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
 /// 设置一个已访问的构建块作为快速部件插入到文档中，并将文本添加到其内容中。
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
         // 将 Building Block 配置为快速部件，并添加 Building Blocks Organizer 使用的属性。
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

         // 添加一个带有文本的部分。
         // 将块插入到文档中会在 location.
 处附加该部分及其子节点
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

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
