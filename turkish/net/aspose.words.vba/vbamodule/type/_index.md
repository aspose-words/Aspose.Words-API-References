---
title: VbaModule.Type
second_title: Aspose.Words for .NET API Referansı
description: VbaModule mülk. Modülün bir prosedür modülü belge modülü sınıf modülü veya tasarımcı modülü olup olmadığını belirtir.
type: docs
weight: 40
url: /tr/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Modülün bir prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir.

```csharp
public VbaModuleType Type { get; set; }
```

### Örnekler

Makroları kullanarak bir VBA projesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Yeni bir VBA projesi oluşturun.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Yeni bir modül oluşturun ve bir makro kaynak kodu belirleyin.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modülü VBA projesine ekleyin.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Ayrıca bakınız

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* ad alanı [Aspose.Words.Vba](../../vbamodule/)
* toplantı [Aspose.Words](../../../)


