---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words for .NET
description: Aspose.Words.Vba.VbaProject sınıf. VBA proje bilgilerine erişim sağlar. Belge içindeki bir VBA projesi VBA modüllerinin bir koleksiyonu olarak tanımlanır C#'da.
type: docs
weight: 6580
url: /tr/net/aspose.words.vba/vbaproject/
---
## VbaProject class

VBA proje bilgilerine erişim sağlar. Belge içindeki bir VBA projesi, VBA modüllerinin bir koleksiyonu olarak tanımlanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışmak](https://docs.aspose.com/words/net/working-with-vba-macros/) dokümantasyon makalesi.

```csharp
public class VbaProject
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [VbaProject](vbaproject/)() | Bir boşluk oluşturur`VbaProject` . |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | VBA projesinin kod sayfasını alır veya ayarlar. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Şunun olup olmadığını gösterir:`VbaProject` imzalanmış veya imzalanmamış. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | VBA proje modüllerinin koleksiyonunu döndürür. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | VBA proje adını alır veya ayarlar. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | VBA proje referanslarının bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Bir kopyasını gerçekleştirir`VbaProject` . |

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

// VBA modülü için yeni kaynak kodunu ayarlayın. Koleksiyondaki VBA modüllerine dizine veya isme göre erişebilirsiniz.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Koleksiyondan bir modülü kaldırın.
vbaModules.Remove(vbaModules[2]);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)
