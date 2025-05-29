---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words for .NET
description: 解锁 Aspose.Words.Vba.VbaModule 的强大功能，无缝访问您的 VBA 项目模块。提高生产力并简化您的文档自动化！
type: docs
weight: 7400
url: /zh/net/aspose.words.vba/vbamodule/
---
## VbaModule class

提供对 VBA 项目模块的访问。

要了解更多信息，请访问[使用 VBA 宏](https://docs.aspose.com/words/net/working-with-vba-macros/)文档文章。

```csharp
public class VbaModule
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [VbaModule](vbamodule/)() | 创建一个空模块。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | 获取或设置 VBA 项目模块名称。 |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | 获取或设置 VBA 项目模块源代码。 |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | 指定模块是过程模块、文档模块、类模块还是设计器模块。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | 执行复制`VbaModule`. |

## 例子

展示如何访问文档的 VBA 项目信息。

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// VBA 项目包含 VBA 模块的集合。
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules;

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// 为 VBA 模块设置新的源代码。您可以通过索引或名称访问集合中的 VBA 模块。
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// 从集合中删除一个模块。
vbaModules.Remove(vbaModules[2]);
```

### 也可以看看

* 命名空间 [Aspose.Words.Vba](../../aspose.words.vba/)
* 部件 [Aspose.Words](../../)
