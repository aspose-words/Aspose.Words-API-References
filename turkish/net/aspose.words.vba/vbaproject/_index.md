---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: .NET için Aspose.Words
description: Belgelerinizdeki VBA proje bilgilerini ve modüllerini zahmetsizce yönetmek için Aspose.Words.Vba.VbaProject sınıfının gücünü açığa çıkarın. Otomasyonunuzu bugün geliştirin!
type: docs
weight: 7430
url: /tr/net/aspose.words.vba/vbaproject/
---
## VbaProject class

VBA proje bilgilerine erişim sağlar. Belge içindeki bir VBA projesi, VBA modülleri koleksiyonu olarak tanımlanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışma](https://docs.aspose.com/words/net/working-with-vba-macros/) belgeleme makalesi.

```csharp
public class VbaProject
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [VbaProject](vbaproject/)() | Boş bir sayfa oluşturur`VbaProject` . |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | VBA projesinin kod sayfasını alır veya ayarlar. |
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | Aşağıdakilerin olup olmadığını gösterir:`VbaProject` şifre korumalıdır. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Aşağıdakilerin olup olmadığını gösterir:`VbaProject` imzalanmış mı değil mi? |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | VBA proje modülleri koleksiyonunu döndürür. |
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

// VBA modülü için yeni kaynak kodu ayarlayın. Koleksiyondaki VBA modüllerine dizine veya adına göre erişebilirsiniz.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Koleksiyondan bir modülü kaldır.
vbaModules.Remove(vbaModules[2]);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)
