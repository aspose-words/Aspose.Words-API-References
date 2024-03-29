---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Vba.VbaModuleCollection sınıf. Aşağıdakilerin bir koleksiyonunu temsil ederVbaModule nesneler C#'da.
type: docs
weight: 6560
url: /tr/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Aşağıdakilerin bir koleksiyonunu temsil eder:[`VbaModule`](../vbamodule/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışmak](https://docs.aspose.com/words/net/working-with-vba-macros/) dokümantasyon makalesi.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Koleksiyondaki VBA modüllerinin sayısını döndürür. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Bir öğeyi alır[`VbaModule`](../vbamodule/) indekse göre nesne. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | Koleksiyona bir modül ekler. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | Belirtilen modülü koleksiyondan kaldırır. |

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

* class [VbaModule](../vbamodule/)
* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)
