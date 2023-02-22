---
title: Class VbaModuleCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Vba.VbaModuleCollection klas. Repräsentiert eine Sammlung vonVbaModule Objekte.
type: docs
weight: 6250
url: /de/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Repräsentiert eine Sammlung von[`VbaModule`](../vbamodule/) Objekte.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Gibt die Anzahl der VBA-Module in der Sammlung zurück. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Ruft a[`VbaModule`](../vbamodule/) Objekt nach Index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | Fügt der Sammlung ein Modul hinzu. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | Entfernt das angegebene Modul aus der Sammlung. |

### Beispiele

Zeigt, wie auf die VBA-Projektinformationen eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Ein VBA-Projekt enthält eine Sammlung von VBA-Modulen.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Neuen Quellcode für VBA-Modul setzen. Sie können auf VBA-Module in der Sammlung entweder nach Index oder nach Name zugreifen.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Ein Modul aus der Sammlung entfernen.
vbaModules.Remove(vbaModules[2]);
```

### Siehe auch

* class [VbaModule](../vbamodule/)
* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)


