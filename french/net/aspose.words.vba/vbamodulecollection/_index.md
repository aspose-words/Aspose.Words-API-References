---
title: Class VbaModuleCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Vba.VbaModuleCollection classe. Représente une collection deVbaModule objets.
type: docs
weight: 6250
url: /fr/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Représente une collection de[`VbaModule`](../vbamodule/) objets.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Renvoie le nombre de modules VBA dans la collection. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Récupère un[`VbaModule`](../vbamodule/) objet par index. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | Ajoute un module à la collection. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | Supprime le module spécifié de la collection. |

### Exemples

Montre comment accéder aux informations de projet VBA d'un document.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Un projet VBA contient une collection de modules VBA.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Définit le nouveau code source pour le module VBA. Vous pouvez accéder aux modules VBA de la collection par index ou par nom.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Supprime un module de la collection.
vbaModules.Remove(vbaModules[2]);
```

### Voir également

* class [VbaModule](../vbamodule/)
* espace de noms [Aspose.Words.Vba](../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../)


