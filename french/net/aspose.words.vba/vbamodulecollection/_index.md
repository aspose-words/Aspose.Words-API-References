---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Vba.VbaModuleCollection, votre outil indispensable pour gérer efficacement les objets VbaModule dans l'automatisation des documents.
type: docs
weight: 7410
url: /fr/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Représente une collection de[`VbaModule`](../vbamodule/) objets.

Pour en savoir plus, visitez le[Travailler avec les macros VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) article de documentation.

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
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | Ajoute un module à la collection. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | Supprime le module spécifié de la collection. |

## Exemples

Montre comment accéder aux informations du projet VBA d'un document.

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

// Définition du nouveau code source du module VBA. Vous pouvez accéder aux modules VBA de la collection par index ou par nom.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Supprimer un module de la collection.
vbaModules.Remove(vbaModules[2]);
```

### Voir également

* class [VbaModule](../vbamodule/)
* espace de noms [Aspose.Words.Vba](../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../)
