---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: VbaModuleCollection Add méthode. Ajoute un module à la collection en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Ajoute un module à la collection.

```csharp
public void Add(VbaModule vbaModule)
```

## Exemples

Montre comment créer un projet VBA à l'aide de macros.

```csharp
Document doc = new Document();

// Créez un nouveau projet VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Créez un nouveau module et spécifiez un code source de macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Ajoute le module au projet VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Voir également

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espace de noms [Aspose.Words.Vba](../../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../../)
