---
title: VbaProject.IsProtected
linktitle: IsProtected
articleTitle: IsProtected
second_title: Aspose.Words for .NET
description: 使用 IsProtected 属性检查您的 VbaProject 是否受密码保护。确保代码安全并有效简化项目管理！
type: docs
weight: 30
url: /zh/net/aspose.words.vba/vbaproject/isprotected/
---
## VbaProject.IsProtected property

显示[`VbaProject`](../)受密码保护。

```csharp
public bool IsProtected { get; }
```

## 例子

显示 VbaProject 是否受密码保护。

```csharp
Document doc = new Document(MyDir + "Vba protected.docm");
Assert.True(doc.VbaProject.IsProtected);
```

### 也可以看看

* class [VbaProject](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
