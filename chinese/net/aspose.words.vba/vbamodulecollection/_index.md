---
title: VbaModuleCollection
second_title: Aspose.Words for .NET API 参考
description: 代表一个集合VbaModule./vbamodule对象.
type: docs
weight: 6250
url: /zh/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

代表一个集合[`VbaModule`](../vbamodule)对象.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count) { get; } | 返回集合中 VBA 模块的数量。 |
| [Item](../../aspose.words.vba/vbamodulecollection/item) { get; } | 检索一个[`VbaModule`](../vbamodule)按索引的对象. (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add)(VbaModule) | 将模块添加到集合中。 |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove)(VbaModule) | 从集合中删除指定的模块。 |

### 例子

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

* class [VbaModule](../vbamodule)
* 命名空间 [Aspose.Words.Vba](../../aspose.words.vba)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
