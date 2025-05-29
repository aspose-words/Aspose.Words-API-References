---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words for .NET
description: 使用 FileFormatInfo HasMacros 属性检查您的文档是否包含 VBA 宏。立即确保文档的安全性和功能！
type: docs
weight: 30
url: /zh/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

返回`真的`如果此文档包含 VBA 宏。

```csharp
public bool HasMacros { get; }
```

## 例子

展示如何在不加载文档的情况下检查 VBA 宏的存在。

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### 也可以看看

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
