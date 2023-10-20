---
title: VbaProject.CodePage
linktitle: CodePage
articleTitle: CodePage
second_title: Aspose.Words pour .NET
description: VbaProject CodePage propriété. Obtient ou définit la page de codes du projet VBA en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Obtient ou définit la page de codes du projet VBA.

```csharp
public int CodePage { get; set; }
```

## Remarques

Veuillez noter que VBA est une fonctionnalité pré-Unicode et que vous devez définir explicitement la page de code appropriée pour préserver les jeux de caractères régionaux.

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

* class [VbaProject](../)
* espace de noms [Aspose.Words.Vba](../../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../../)
