---
title: Document.VbaProject
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient ou définit unVbaProject .
type: docs
weight: 450
url: /fr/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

Obtient ou définit un`VbaProject` .

```csharp
public VbaProject VbaProject { get; set; }
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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


