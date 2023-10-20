---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: 用于 .NET 的 Aspose.Words
description: VbaModule Clone 方法. 执行复制VbaModule 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

执行复制[`VbaModule`](../).

```csharp
public VbaModule Clone()
```

### 返回值

克隆人[`VbaModule`](../)。

## 例子

演示如何深度克隆 VBA 项目和模块。

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// 在目标文档中，我们已经有一个名为“Module1”的模块
// 因为我们将它与项目一起克隆。我们需要删除该模块。
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### 也可以看看

* class [VbaModule](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
