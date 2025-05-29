---
title: OfficeMath Class
linktitle: OfficeMath
articleTitle: OfficeMath
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Math.OfficeMath 类，旨在轻松创建和管理方程式和矩阵等 Office Math 对象。
type: docs
weight: 4810
url: /zh/net/aspose.words.math/officemath/
---
## OfficeMath class

表示 Office Math 对象，例如函数、方程式、矩阵等。可包含子元素 ，包括数学文本、书签、注释和其他`OfficeMath`实例和一些其他节点。

要了解更多信息，请访问[使用 OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/)文档文章。

```csharp
public class OfficeMath : CompositeNode
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | 获取/设置 Office Math 显示格式类型，表示公式是否与文本内联显示或显示在自己的行上。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | 获取/设置 Office Math 对齐。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | 获取类型[`MathObjectType`](./mathobjecttype/)此 Office Math 对象的 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | 返回OfficeMath. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.math/officemath/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客参观办公室数学的结束。 |
| override [AcceptStart](../../aspose.words.math/officemath/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客参观办公室数学的开始。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | 创建并返回一个可用于将此方程式渲染为图像的对象。 |
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

在此版本的 Aspose.Words 中，`OfficeMath`节点不提供公共方法 和属性来创建或修改`OfficeMath`对象。在此版本中，您无法实例化 Math节点或修改现有节点（删除它们除外）。

`OfficeMath`只能是[`Paragraph`](../../aspose.words/paragraph/)。

## 例子

展示如何设置办公室数学显示格式。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// 作为其他 OfficeMath 节点的子节点的 OfficeMath 节点始终是内联的。
// 我们正在处理的节点是改变其位置和显示类型的基础节点。
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// 更改OfficeMath节点的位置和显示类型。
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### 也可以看看

* class [CompositeNode](../../aspose.words/compositenode/)
* 命名空间 [Aspose.Words.Math](../../aspose.words.math/)
* 部件 [Aspose.Words](../../)
