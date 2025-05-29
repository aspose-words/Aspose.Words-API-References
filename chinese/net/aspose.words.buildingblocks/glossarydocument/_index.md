---
title: GlossaryDocument Class
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.BuildingBlocks.GlossaryDocument 类，这是在 Word 文档中无缝管理自动图文集和构建块的关键。
type: docs
weight: 370
url: /zh/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

表示 Word 文档中词汇表文档的根元素。 词汇表文档是自动图文集、自动更正条目和构建块的存储。

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class GlossaryDocument : DocumentBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | 获取或设置文档的背景形状。可以是`无效的`. |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | 返回代表词汇表文档中所有构建块的类型集合。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| override [Document](../../aspose.words/documentbase/document/) { get; } | 获取此实例。 |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | 获取词汇表文档中的第一个构建块。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | 提供对本文档中使用的字体属性的访问。 |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | 提供对文档中定义的脚注/尾注分隔符的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | 获取词汇表文档中的最后一个构建块。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | 提供对文档中使用的列表格式的访问。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | 在文档中插入或删除节点时调用。 |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | 返回GlossaryDocument值. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | 获取或设置文档的页面颜色。此属性是[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/). |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | 允许控制如何加载外部资源。 |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | 返回文档中定义的样式集合。 |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | 在各种文档处理过程中，当检测到可能导致数据或格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访问者访问词汇表文档的末尾。 |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访问者访问词汇表文档的开头。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(*[BuildingBlockGallery](../buildingblockgallery/), string, string*) | 使用指定的图库、类别和名称查找构建块。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool*) | 将节点从另一个文档导入到当前文档。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool, [ImportFormatMode](../../aspose.words/importformatmode/)*) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
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

一些文档（通常是模板）可以包含自动图文集、自动更正条目 和/或构建块（也称为词汇表文档条目，文档部分 或构建块）。

要访问构建块，您需要将文档加载到[`Document`](../../aspose.words/document/) 对象。构建块将通过[`GlossaryDocument`](../../aspose.words/document/glossarydocument/)财产。

`GlossaryDocument`可以包含任意数量的[`BuildingBlock`](../buildingblock/)对象. 每个[`BuildingBlock`](../buildingblock/)代表一个文档部分。

对应于**词汇表文档**和**文档部分**OOXML 中的元素。

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

* class [DocumentBase](../../aspose.words/documentbase/)
* 命名空间 [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* 部件 [Aspose.Words](../../)
