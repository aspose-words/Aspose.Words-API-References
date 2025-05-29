---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: .NET için Aspose.Words
description: Oluşturucu aracımızla zahmetsizce yeni bir VbaProject oluşturun. Programlama yolculuğunuza boş bir projeyle başlayın ve yaratıcılığınızı serbest bırakın!
type: docs
weight: 10
url: /tr/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Boş bir sayfa oluşturur[`VbaProject`](../) .

```csharp
public VbaProject()
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

### Ayrıca bakınız

* class [VbaProject](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
