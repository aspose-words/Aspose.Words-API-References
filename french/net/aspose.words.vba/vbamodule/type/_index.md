---
title: VbaModule.Type
second_title: Référence de l'API Aspose.Words pour .NET
description: VbaModule propriété. Spécifie si le module est un module procédural un module de document un module de classe ou un module de concepteur.
type: docs
weight: 40
url: /fr/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Spécifie si le module est un module procédural, un module de document, un module de classe ou un module de concepteur.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* espace de noms [Aspose.Words.Vba](../../vbamodule/)
* Assemblée [Aspose.Words](../../../)


