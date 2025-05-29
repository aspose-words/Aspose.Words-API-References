---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: VbaModule Type özelliğini keşfedin, gelişmiş işlevsellik ve organizasyon için modüllerinizi prosedürel, belge, sınıf veya tasarımcı olarak tanımlayın.
type: docs
weight: 40
url: /tr/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Modülün prosedürel modül, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
