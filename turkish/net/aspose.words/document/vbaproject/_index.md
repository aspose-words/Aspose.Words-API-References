---
title: Document.VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: .NET için Aspose.Words
description: VbaProject özelliklerini etkili bir şekilde nasıl yöneteceğinizi keşfedin. Gelişmiş otomasyon ve akıcı iş akışları için VbaProject'i nasıl alacağınızı veya ayarlayacağınızı öğrenin.
type: docs
weight: 470
url: /tr/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

Bir değeri alır veya ayarlar`VbaProject` .

```csharp
public VbaProject VbaProject { get; set; }
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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
