---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words for .NET
description: 使用我们的构造函数工具轻松创建一个新的 VbaProject。从空白项目开启您的编程之旅，释放您的创造力！
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

* class [VbaProject](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
