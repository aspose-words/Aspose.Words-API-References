---
title: VbaModuleCollection.Remove
second_title: Aspose.Words für .NET-API-Referenz
description: VbaModuleCollection methode. Entfernt das angegebene Modul aus der Sammlung.
type: docs
weight: 40
url: /de/net/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection.Remove method

Entfernt das angegebene Modul aus der Sammlung.

```csharp
public void Remove(VbaModule module)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| module | VbaModule | Das zu entfernende Modul. |

### Beispiele

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

// Ein Modul aus der Sammlung entfernen.
vbaModules.Remove(vbaModules[2]);
```

### Siehe auch

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namensraum [Aspose.Words.Vba](../../vbamodulecollection/)
* Montage [Aspose.Words](../../../)


