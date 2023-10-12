---
title: VbaModuleCollection.Remove
second_title: Aspose.Words for .NET API Referansı
description: VbaModuleCollection yöntem. Belirtilen modülü koleksiyondan kaldırır.
type: docs
weight: 40
url: /tr/net/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection.Remove method

Belirtilen modülü koleksiyondan kaldırır.

```csharp
public void Remove(VbaModule module)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| module | VbaModule | Kaldırılacak modül. |

### Örnekler

Bir belgenin VBA proje bilgilerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Bir VBA projesi, VBA modüllerinin bir koleksiyonunu içerir.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// VBA modülü için yeni kaynak kodunu ayarlayın. Koleksiyondaki VBA modüllerine dizine veya isme göre erişebilirsiniz.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Koleksiyondan bir modülü kaldırın.
vbaModules.Remove(vbaModules[2]);
```

### Ayrıca bakınız

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* ad alanı [Aspose.Words.Vba](../../vbamodulecollection/)
* toplantı [Aspose.Words](../../../)


