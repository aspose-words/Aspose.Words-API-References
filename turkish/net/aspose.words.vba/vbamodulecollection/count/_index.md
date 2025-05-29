---
title: VbaModuleCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: VBA modüllerinizi verimli bir şekilde sayan, kodlama iş akışınızı ve organizasyonunuzu geliştiren VbaModuleCollection Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.vba/vbamodulecollection/count/
---
## VbaModuleCollection.Count property

Koleksiyondaki VBA modüllerinin sayısını döndürür.

```csharp
public int Count { get; }
```

## Örnekler

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

// VBA modülü için yeni kaynak kodu ayarlayın. Koleksiyondaki VBA modüllerine dizine veya adına göre erişebilirsiniz.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Koleksiyondan bir modülü kaldır.
vbaModules.Remove(vbaModules[2]);
```

### Ayrıca bakınız

* class [VbaModuleCollection](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
