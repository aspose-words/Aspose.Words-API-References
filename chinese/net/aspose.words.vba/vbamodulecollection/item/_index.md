---
title: VbaModuleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 使用 VbaModuleCollection Item 属性轻松访问 VbaModule 对象。通过轻松索引和改进的管理功能增强您的 VBA 项目。
type: docs
weight: 20
url: /zh/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

检索[`VbaModule`](../../vbamodule/)按索引排序的对象.

```csharp
public VbaModule this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 要检索的模块的从零开始的索引。 |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

检索[`VbaModule`](../../vbamodule/)按名称返回对象，如果未找到则返回 Null。

```csharp
public VbaModule this[string name] { get; }
```

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
