---
title: VbaModule.VbaModule
second_title: Aspose.Words for .NET API Referansı
description: VbaModule inşaatçı. Boş bir modül oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Boş bir modül oluşturur.

```csharp
public VbaModule()
```

### Örnekler

Makroları kullanarak bir VBA projesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Yeni bir VBA projesi oluşturun.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Yeni bir modül oluşturun ve bir makro kaynak kodu belirtin.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modülü VBA projesine ekleyin.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Ayrıca bakınız

* class [VbaModule](../)
* ad alanı [Aspose.Words.Vba](../../vbamodule/)
* toplantı [Aspose.Words](../../../)


