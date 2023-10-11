---
title: Class VbaModule
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Vba.VbaModule sınıf. VBA proje modülüne erişim sağlar.
type: docs
weight: 6550
url: /tr/net/aspose.words.vba/vbamodule/
---
## VbaModule class

VBA proje modülüne erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışmak](https://docs.aspose.com/words/net/working-with-vba-macros/) dokümantasyon makalesi.

```csharp
public class VbaModule
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [VbaModule](vbamodule/)() | Boş bir modül oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | VBA proje modülü adını alır veya ayarlar. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | VBA proje modülü kaynak kodunu alır veya ayarlar. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Bir kopyasını gerçekleştirir`VbaModule` . |

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

* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)


