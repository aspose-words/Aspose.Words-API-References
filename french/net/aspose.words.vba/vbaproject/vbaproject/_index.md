---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words pour .NET
description: Créez facilement un nouveau projet VBA grâce à notre outil de création. Commencez votre parcours de programmation avec un projet vierge et laissez libre cours à votre créativité !
type: docs
weight: 10
url: /fr/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Crée un espace vide[`VbaProject`](../) .

```csharp
public VbaProject()
```

## Exemples

Montre comment créer un projet VBA à l'aide de macros.

```csharp
Document doc = new Document();

// Créer un nouveau projet VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Créez un nouveau module et spécifiez un code source de macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Ajoutez le module au projet VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Voir également

* class [VbaProject](../)
* espace de noms [Aspose.Words.Vba](../../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../../)
