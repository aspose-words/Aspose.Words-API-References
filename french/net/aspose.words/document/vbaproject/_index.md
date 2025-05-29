---
title: Document.VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer efficacement les propriétés de VbaProject. Apprenez à obtenir ou à configurer VbaProject pour une automatisation améliorée et des workflows simplifiés.
type: docs
weight: 470
url: /fr/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

Obtient ou définit un`VbaProject` .

```csharp
public VbaProject VbaProject { get; set; }
```

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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
