---
title: VbaProject.VbaProject
second_title: Aspose.Words for .NET API Referansı
description: VbaProject inşaatçı. Boş bir VbaProject oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Boş bir VbaProject oluşturur.

```csharp
public VbaProject()
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

* class [VbaProject](../)
* ad alanı [Aspose.Words.Vba](../../vbaproject/)
* toplantı [Aspose.Words](../../../)


