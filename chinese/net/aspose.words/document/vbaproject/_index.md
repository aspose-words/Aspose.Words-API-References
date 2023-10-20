---
title: Document.VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: 用于 .NET 的 Aspose.Words
description: Document VbaProject 财产. 获取或设置VbaProject 在 C#.
type: docs
weight: 450
url: /zh/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

获取或设置`VbaProject`.

```csharp
public VbaProject VbaProject { get; set; }
```

## 例子

演示如何访问文档的 VBA 项目信息。

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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
