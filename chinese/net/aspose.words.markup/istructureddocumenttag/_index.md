---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.IStructuredDocumentTag 界面，以便高效管理结构化文档标签并增强您的文档处理能力！
type: docs
weight: 4660
url: /zh/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

接口定义通用数据[`StructuredDocumentTag`](../structureddocumenttag/)和[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/).

```csharp
public interface IStructuredDocumentTag
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | 获取或设置结构化文档标签的外观。 |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | 指定一个唯一的只读持久数字 ID**特殊和差别待遇**。 |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | 如果此实例是范围（多部分）结构化文档标签，则返回 true。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | 指定此内容是否**特殊和差别待遇**应解释为包含占位符文本 （与 SDT 中的常规文本内容相反）。 |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | 获取此**特殊和差别待遇**出现在文档树中。 |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | 设置为 true 时，此属性将禁止用户删除此**特殊和差别待遇**. |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | 设置为 true 时，此属性将禁止用户编辑此内容**特殊和差别待遇**. |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | 返回实现此接口的 Node 对象。 |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含当此 SDT 运行内容为空时应显示的占位符文本， 关联的映射 XML 元素为空，如通过[`XmlMapping`](./xmlmapping/)element 或[`IsShowingPlaceholderText`](./isshowingplaceholdertext/)元素为真。 |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | 获取或设置[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。 |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | 获取此类型**结构化文档标签**. |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | 指定与当前 SDT 节点关联的标签。 不能为空。 |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | 指定与此相关的友好名称**特殊和差别待遇** . 不能为空。 |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | 获取一个对象，该对象表示此结构化文档标签到当前文档的自定义 XML 部分中的 XML 数据的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | 仅删除此 SDT 节点本身，但保留其在文档树中的内容。 |

## 例子

展示如何删除结构化文档标签，但保留其中的内容。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // 此集合提供了用于访问范围和非范围结构化标签的统一接口。
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// 这里我们可以从范围和非范围结构化标签的公共接口中获取子节点。
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
