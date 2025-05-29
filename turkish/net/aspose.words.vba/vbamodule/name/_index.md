---
title: VbaModule.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Gelişmiş organizasyon ve verimlilik için VBA proje modül adlarınızı kolayca yönetmek amacıyla VbaModule Name özelliğinin nasıl kullanılacağını keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.vba/vbamodule/name/
---
## VbaModule.Name property

VBA proje modül adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Örnekler

Makrolar kullanılarak bir VBA projesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Yeni bir VBA projesi oluşturun.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Yeni bir modül oluştur ve bir makro kaynak kodu belirt.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modülü VBA projesine ekleyin.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

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

* class [VbaModule](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
