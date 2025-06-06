---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Vba.VbaModuleType 枚举，定义 VBA 项目中的模型类型，以增强自动化和简化文档管理。
type: docs
weight: 7420
url: /zh/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

指定 VBA 项目中模型的类型。

```csharp
public enum VbaModuleType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| DocumentModule | `0` | 一种 VBA 项目项，用于指定与文档关联的嵌入宏和编程访问操作 的模块。 |
| ProceduralModule | `1` | 子程序和函数的集合。 |
| ClassModule | `2` | 包含新对象定义的模块。每个类的实例都会创建一个新对象， 并且模块中定义的过程将成为该对象的属性和方法。 |
| DesignerModule | `3` | 一个 VBA 模块，它扩展了已在项目中注册的 ActiveX 控件的方法和属性。 |

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

* 命名空间 [Aspose.Words.Vba](../../aspose.words.vba/)
* 部件 [Aspose.Words](../../)
