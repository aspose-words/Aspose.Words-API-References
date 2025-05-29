---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words for .NET
description: 使用 LoadOptions 的 ConvertShapeToOfficeMath 属性轻松地将带有 EquationXML 的形状转换为 Office Math 对象，以增强文档的清晰度。
type: docs
weight: 40
url: /zh/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

获取或设置是否将带有 EquationXML 的形状转换为 Office Math 对象。

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## 例子

展示如何将 EquationXML 形状转换为 Office Math 对象。

```csharp
LoadOptions loadOptions = new LoadOptions();

// 使用此标志指定是否转换具有 EquationXML 属性的形状
// 到 Office Math 对象，然后加载文档。
loadOptions.ConvertShapeToOfficeMath = isConvertShapeToOfficeMath;

Document doc = new Document(MyDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    Assert.AreEqual(16, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(34, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
else
{
    Assert.AreEqual(24, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(0, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
