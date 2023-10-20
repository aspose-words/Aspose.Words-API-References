---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: 用于 .NET 的 Aspose.Words
description: VbaProject 构造函数. 创建一个空白VbaProject 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

创建一个空白[`VbaProject`](../).

```csharp
public VbaProject()
```

## 例子

演示如何使用宏创建 VBA 项目。

```csharp
Document doc = new Document();

// 创建一个新的 VBA 项目。
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// 创建一个新模块并指定宏源代码。
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// 将模块添加到 VBA 项目中。
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### 也可以看看

* class [VbaProject](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
