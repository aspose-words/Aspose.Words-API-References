---
title: VbaModuleCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: Supprimez facilement des modules spécifiques de votre collection VBAModuleCollection grâce à notre méthode de suppression facile à utiliser. Simplifiez vos projets VBA dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection.Remove method

Supprime le module spécifié de la collection.

```csharp
public void Remove(VbaModule module)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| module | VbaModule | Le module à supprimer. |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espace de noms [Aspose.Words.Vba](../../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../../)
