---
title: VbaProject.CodePage
second_title: Référence de l'API Aspose.Words pour .NET
description: VbaProject propriété. Renvoie la page de code du projet VBA.
type: docs
weight: 20
url: /fr/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Renvoie la page de code du projet VBA.

```csharp
public int CodePage { get; }
```

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

* class [VbaProject](../)
* espace de noms [Aspose.Words.Vba](../../vbaproject/)
* Assemblée [Aspose.Words](../../../)


