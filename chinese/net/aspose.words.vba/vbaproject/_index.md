---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Vba.VbaProject 班级. 提供对 VBA 项目信息的访问 文档中的 VBA 项目被定义为 VBA 模块的集合 在 C#.
type: docs
weight: 6580
url: /zh/net/aspose.words.vba/vbaproject/
---
## VbaProject class

提供对 VBA 项目信息的访问。 文档中的 VBA 项目被定义为 VBA 模块的集合。

```csharp
public class VbaProject
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [VbaProject](vbaproject/)() | 创建一个空白 VbaProject. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | 返回 VBA 项目的代码页。 |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | 显示 VbaProject 是否已签名。 |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | 返回 VBA 项目模块的集合。 |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | 获取或设置 VBA 项目名称。 |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | 获取 VBA 项目引用的集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | 执行`VbaProject`. |

## 例子

显示如何访问文档的 VBA 项目信息。

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// VBA 项目包含 VBA 模块的集合。
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// 为 VBA 模块设置新的源代码。您可以通过索引或名称访问集合中的 VBA 模块。
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// 从集合中移除一个模块。
vbaModules.Remove(vbaModules[2]);
```

### 也可以看看

* 命名空间 [Aspose.Words.Vba](../../aspose.words.vba/)
* 部件 [Aspose.Words](../../)
