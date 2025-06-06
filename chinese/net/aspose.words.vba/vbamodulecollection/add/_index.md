---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 使用 VbaModuleCollection Add 方法轻松增强您的 VBA 项目，允许无缝添加模块以改进功能。
type: docs
weight: 30
url: /zh/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

将模块添加到集合中。

```csharp
public void Add(VbaModule vbaModule)
```

## 例子

展示如何使用宏创建 VBA 项目。

```csharp
Document doc = new Document();

// 创建一个新的 VBA 项目。
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// 创建一个新模块并指定一个宏源代码。
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// 将模块添加到 VBA 项目。
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### 也可以看看

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
