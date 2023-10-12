---
title: VbaModuleCollection.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: VbaModuleCollection propriété. Récupère unVbaModule objet par index.
type: docs
weight: 20
url: /fr/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

Récupère un[`VbaModule`](../../vbamodule/) objet par index.

```csharp
public VbaModule this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Index de base zéro du module à récupérer. |

### Exemples

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espace de noms [Aspose.Words.Vba](../../vbamodulecollection/)
* Assemblée [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

Récupère un[`VbaModule`](../../vbamodule/) objet par nom, ou Null s'il n'est pas trouvé.

```csharp
public VbaModule this[string name] { get; }
```

### Exemples

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espace de noms [Aspose.Words.Vba](../../vbamodulecollection/)
* Assemblée [Aspose.Words](../../../)


