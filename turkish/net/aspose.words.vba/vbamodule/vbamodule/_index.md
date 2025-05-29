---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: .NET için Aspose.Words
description: VbaModule oluşturucumuzla boş VBA modüllerini zahmetsizce oluşturun. Kodlama sürecinizi kolaylaştırın ve geliştirme iş akışınızı bugün geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Boş bir modül oluşturur.

```csharp
public VbaModule()
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

* class [VbaModule](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
