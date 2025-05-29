---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: 使用 Clone 方法轻松复制您的 VbaProject。立即增强您的工作流程并简化项目管理！
type: docs
weight: 80
url: /zh/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

执行复制[`VbaProject`](../).

```csharp
public VbaProject Clone()
```

### 返回值

克隆人[`VbaProject`](../)。

## 例子

展示如何深度克隆 VBA 项目和模块。

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// 在目标文档中，我们已经有一个名为“Module1”的模块
// 因为我们把它和项目一起克隆了。我们需要删除这个模块。
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### 也可以看看

* class [VbaProject](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
