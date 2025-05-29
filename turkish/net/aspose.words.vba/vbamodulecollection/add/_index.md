---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: VbaModuleCollection Add yöntemi ile VBA projelerinizi zahmetsizce geliştirin ve işlevselliği artırmak için modüllerin sorunsuz bir şekilde eklenmesine olanak tanıyın.
type: docs
weight: 30
url: /tr/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Koleksiyona bir modül ekler.

```csharp
public void Add(VbaModule vbaModule)
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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
