---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words for .NET
description: 使用 FieldEQ 的 AsOfficeMath 方法转换 EQ 字段，轻松将它们转换为 Office Math 对象，实现无缝文档集成。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

返回与 EQ 字段对应的 Office Math 对象。

```csharp
public OfficeMath AsOfficeMath()
```

### 返回值

返回`无效的`如果字段代码为空或无效，否则[`OfficeMath`](../../../aspose.words.math/officemath/)实例.

## 例子

展示如何用 Office Math 替换 EQ 字段。

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### 也可以看看

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
