---
title: VbaProject.IsSigned
linktitle: IsSigned
articleTitle: IsSigned
second_title: .NET için Aspose.Words
description: Proje imzalarını kolayca doğrulamak ve kod güvenliğinizi artırmak için VbaProject IsSigned özelliğini keşfedin. VBA projelerinizin güvenilir olduğundan emin olun!
type: docs
weight: 40
url: /tr/net/aspose.words.vba/vbaproject/issigned/
---
## VbaProject.IsSigned property

Aşağıdakilerin olup olmadığını gösterir:[`VbaProject`](../) imzalanmış mı değil mi?

```csharp
public bool IsSigned { get; }
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

* class [VbaProject](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
