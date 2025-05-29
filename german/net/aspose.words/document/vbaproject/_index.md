---
title: Document.VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie VbaProject-Eigenschaften effektiv verwalten. Erfahren Sie, wie Sie VbaProject für verbesserte Automatisierung und optimierte Arbeitsabläufe abrufen oder festlegen.
type: docs
weight: 470
url: /de/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

Ruft ab oder setzt einen`VbaProject` .

```csharp
public VbaProject VbaProject { get; set; }
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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
