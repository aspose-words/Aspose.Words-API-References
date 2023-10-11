---
title: Class VbaModule
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Vba.VbaModule klas. Bietet Zugriff auf das VBAProjektmodul.
type: docs
weight: 6550
url: /de/net/aspose.words.vba/vbamodule/
---
## VbaModule class

Bietet Zugriff auf das VBA-Projektmodul.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit VBA-Makros](https://docs.aspose.com/words/net/working-with-vba-macros/) Dokumentationsartikel.

```csharp
public class VbaModule
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [VbaModule](vbamodule/)() | Erstellt ein leeres Modul. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | Ruft den VBA-Projektmodulnamen ab oder legt ihn fest. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | Ruft den Quellcode des VBA-Projektmoduls ab oder legt ihn fest. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Gibt an, ob das Modul ein prozedurales Modul, ein Dokumentmodul, ein Klassenmodul oder ein Designermodul ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Führt eine Kopie des aus`VbaModule` . |

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

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)


