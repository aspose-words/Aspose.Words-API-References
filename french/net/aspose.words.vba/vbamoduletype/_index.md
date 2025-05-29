---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Vba.VbaModuleType, définissant les types de modèles dans les projets VBA pour une automatisation améliorée et une gestion simplifiée des documents.
type: docs
weight: 7420
url: /fr/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Spécifie le type d'un modèle dans un projet VBA.

```csharp
public enum VbaModuleType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| DocumentModule | `0` | Un type d'élément de projet VBA qui spécifie un module pour les macros incorporées et les opérations d'accès programmatique qui sont associées à un document. |
| ProceduralModule | `1` | Une collection de sous-routines et de fonctions. |
| ClassModule | `2` | Un module contenant la définition d'un nouvel objet. Chaque instance d'une classe crée un nouvel objet, et les procédures définies dans le module deviennent des propriétés et des méthodes de l'objet. |
| DesignerModule | `3` | Un module VBA qui étend les méthodes et les propriétés d'un contrôle ActiveX qui a été enregistré avec le projet. |

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

* espace de noms [Aspose.Words.Vba](../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../)
