---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: 用于 .NET 的 Aspose.Words
description: OleFormat SuggestedFileName 财产. 如果要将当前嵌入对象保存到文件中则获取建议的文件名 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

如果要将当前嵌入对象保存到文件中，则获取建议的文件名。

```csharp
public string SuggestedFileName { get; }
```

## 例子

演示如何获取 OLE 对象的建议文件名。

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE 对象可以提供建议的文件名和扩展名，
// 将对象的内容保存到本地文件系统中的文件时可以使用它。
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### 也可以看看

* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
