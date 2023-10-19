---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: VbaModuleCollection Add yöntem. Koleksiyona bir modül ekler C#'da.
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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
