---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words pour .NET
description: Aspose.Words.Vba.VbaModule classe. Donne accès au module de projet VBA en C#.
type: docs
weight: 6550
url: /fr/net/aspose.words.vba/vbamodule/
---
## VbaModule class

Donne accès au module de projet VBA.

Pour en savoir plus, visitez le[Travailler avec des macros VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) article documentaire.

```csharp
public class VbaModule
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [VbaModule](vbamodule/)() | Crée un module vide. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | Obtient ou définit le nom du module du projet VBA. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | Obtient ou définit le code source du module de projet VBA. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Spécifie si le module est un module procédural, un module de document, un module de classe ou un module de concepteur. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Effectue une copie du`VbaModule` . |

## Exemples

Montre comment accéder aux informations de projet VBA d’un document.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Un projet VBA contient une collection de modules VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Définir un nouveau code source pour le module VBA. Vous pouvez accéder aux modules VBA de la collection soit par index, soit par nom.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Supprime un module de la collection.
vbaModules.Remove(vbaModules[2]);
```

### Voir également

* espace de noms [Aspose.Words.Vba](../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../)
