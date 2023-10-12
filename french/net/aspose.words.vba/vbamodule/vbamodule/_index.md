---
title: VbaModule.VbaModule
second_title: Référence de l'API Aspose.Words pour .NET
description: VbaModule constructeur. Crée un module vide.
type: docs
weight: 10
url: /fr/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Crée un module vide.

```csharp
public VbaModule()
```

### Exemples

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

* class [VbaModule](../)
* espace de noms [Aspose.Words.Vba](../../vbamodule/)
* Assemblée [Aspose.Words](../../../)


