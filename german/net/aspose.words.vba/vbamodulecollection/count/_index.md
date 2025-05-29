---
title: VbaModuleCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „VbaModuleCollection Count“, die Ihre VBA-Module effizient zählt und so Ihren Codierungsworkflow und Ihre Organisation verbessert.
type: docs
weight: 10
url: /de/net/aspose.words.vba/vbamodulecollection/count/
---
## VbaModuleCollection.Count property

Gibt die Anzahl der VBA-Module in der Sammlung zurück.

```csharp
public int Count { get; }
```

## Beispiele

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

* class [VbaModuleCollection](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
