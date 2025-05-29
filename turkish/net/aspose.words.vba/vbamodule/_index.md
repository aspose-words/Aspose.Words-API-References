---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: .NET için Aspose.Words
description: VBA proje modüllerinize kesintisiz erişim için Aspose.Words.Vba.VbaModule'ün gücünü açığa çıkarın. Üretkenliği artırın ve belge otomasyonunuzu kolaylaştırın!
type: docs
weight: 7400
url: /tr/net/aspose.words.vba/vbamodule/
---
## VbaModule class

VBA proje modülüne erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışma](https://docs.aspose.com/words/net/working-with-vba-macros/) belgeleme makalesi.

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
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | VBA proje modül adını alır veya ayarlar. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | VBA proje modülü kaynak kodunu alır veya ayarlar. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Modülün prosedürel modül, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Bir kopyasını gerçekleştirir`VbaModule` . |

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

* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)
