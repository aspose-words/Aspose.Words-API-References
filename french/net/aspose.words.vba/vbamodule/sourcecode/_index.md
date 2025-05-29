---
title: VbaModule.SourceCode
linktitle: SourceCode
articleTitle: SourceCode
second_title: Aspose.Words pour .NET
description: Accédez et modifiez facilement le code source de vos modules de projet VBA grâce à la propriété VbaModule SourceCode. Améliorez votre efficacité de codage dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.vba/vbamodule/sourcecode/
---
## VbaModule.SourceCode property

Obtient ou définit le code source du module de projet VBA.

```csharp
public string SourceCode { get; set; }
```

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

* class [VbaModule](../)
* espace de noms [Aspose.Words.Vba](../../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../../)
