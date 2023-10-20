---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.Vba.VbaModuleCollection klas. Stellt eine Sammlung von darVbaModule Objekte in C#.
type: docs
weight: 6560
url: /de/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Stellt eine Sammlung von dar[`VbaModule`](../vbamodule/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit VBA-Makros](https://docs.aspose.com/words/net/working-with-vba-macros/) Dokumentationsartikel.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Gibt die Anzahl der VBA-Module in der Sammlung zurück. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Ruft a ab[`VbaModule`](../vbamodule/) Objekt nach index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | Fügt der Sammlung ein Modul hinzu. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | Entfernt das angegebene Modul aus der Sammlung. |

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

// Ein Modul aus der Sammlung entfernen.
vbaModules.Remove(vbaModules[2]);
```

### Siehe auch

* class [VbaModule](../vbamodule/)
* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)
