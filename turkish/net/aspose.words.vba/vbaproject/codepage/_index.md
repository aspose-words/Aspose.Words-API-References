---
title: VbaProject.CodePage
second_title: Aspose.Words for .NET API Referansı
description: VbaProject mülk. VBA projesinin kod sayfasını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

VBA projesinin kod sayfasını alır veya ayarlar.

```csharp
public int CodePage { get; set; }
```

### Notlar

VBA'nın Unicode öncesi bir özellik olduğunu ve bölgesel karakter kümelerini korumak için açıkça uygun kod sayfasını ayarlamanız gerektiğini lütfen unutmayın.

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

* class [VbaProject](../)
* ad alanı [Aspose.Words.Vba](../../vbaproject/)
* toplantı [Aspose.Words](../../../)


