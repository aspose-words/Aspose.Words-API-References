---
title: VbaModule.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft „VbaModule Name“ die Modulnamen Ihres VBA-Projekts einfach verwalten und so für mehr Organisation und Effizienz sorgen können.
type: docs
weight: 20
url: /de/net/aspose.words.vba/vbamodule/name/
---
## VbaModule.Name property

Ruft den VBA-Projektmodulnamen ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

## Beispiele

Zeigt, wie man mit Makros ein VBA-Projekt erstellt.

```csharp
Document doc = new Document();

// Erstellen Sie ein neues VBA-Projekt.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Erstellen Sie ein neues Modul und geben Sie einen Makro-Quellcode an.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Fügen Sie das Modul zum VBA-Projekt hinzu.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

Zeigt, wie auf die VBA-Projektinformationen eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Ein VBA-Projekt enthält eine Sammlung von VBA-Modulen.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules;

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Neuen Quellcode für VBA-Modul festlegen. Sie können auf VBA-Module in der Sammlung entweder über den Index oder über den Namen zugreifen.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Entfernen Sie ein Modul aus der Sammlung.
vbaModules.Remove(vbaModules[2]);
```

### Siehe auch

* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
