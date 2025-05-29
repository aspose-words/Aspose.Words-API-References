---
title: VbaProject.CodePage
linktitle: CodePage
articleTitle: CodePage
second_title: .NET için Aspose.Words
description: Gelişmiş performans ve uyumluluk için VBA projenizin kod sayfası ayarlarını optimize etmek amacıyla VbaProject CodePage özelliğini nasıl yöneteceğinizi keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

VBA projesinin kod sayfasını alır veya ayarlar.

```csharp
public int CodePage { get; set; }
```

## Notlar

Lütfen VBA'nın Unicode öncesi bir özellik olduğunu ve bölgesel karakter kümelerini korumak için uygun kod sayfasını açıkça ayarlamanız gerektiğini unutmayın.

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
