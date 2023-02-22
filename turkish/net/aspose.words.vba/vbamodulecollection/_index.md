---
title: Class VbaModuleCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Vba.VbaModuleCollection sınıf. Bir koleksiyonu temsil ederVbaModule nesneler.
type: docs
weight: 6250
url: /tr/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Bir koleksiyonu temsil eder[`VbaModule`](../vbamodule/) nesneler.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Koleksiyondaki VBA modüllerinin sayısını verir. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Bir[`VbaModule`](../vbamodule/) dizine göre nesne. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | Koleksiyona bir modül ekler. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | Belirtilen modülü koleksiyondan kaldırır. |

### Örnekler

Bir belgenin VBA proje bilgilerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Bir VBA projesi, bir VBA modülleri koleksiyonu içerir.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// VBA modülü için yeni kaynak kodu ayarlayın. Koleksiyondaki VBA modüllerine dizine veya ada göre erişebilirsiniz.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Koleksiyondan bir modülü kaldırın.
vbaModules.Remove(vbaModules[2]);
```

### Ayrıca bakınız

* class [VbaModule](../vbamodule/)
* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)


