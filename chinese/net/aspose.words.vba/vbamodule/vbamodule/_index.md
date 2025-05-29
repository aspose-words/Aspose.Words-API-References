---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words for .NET
description: 使用我们的 VbaModule 构造函数轻松创建空的 VBA 模块。立即简化您的编码流程并增强您的开发工作流程！
type: docs
weight: 10
url: /zh/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

创建一个空模块。

```csharp
public VbaModule()
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

* class [VbaModule](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
