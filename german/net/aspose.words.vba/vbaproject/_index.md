---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words für .NET
description: Nutzen Sie die Leistungsfähigkeit der Aspose.Words.Vba.VbaProject-Klasse, um VBA-Projektinformationen und -Module mühelos in Ihren Dokumenten zu verwalten. Verbessern Sie Ihre Automatisierung noch heute!
type: docs
weight: 7430
url: /de/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Bietet Zugriff auf VBA-Projektinformationen. Ein VBA-Projekt innerhalb des Dokuments wird als Sammlung von VBA-Modulen definiert.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit VBA-Makros](https://docs.aspose.com/words/net/working-with-vba-macros/) Dokumentationsartikel.

```csharp
public class VbaProject
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [VbaProject](vbaproject/)() | Erstellt ein leeres`VbaProject` . |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Ruft die Codepage des VBA-Projekts ab oder legt sie fest. |
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | Zeigt an, ob die`VbaProject` ist passwortgeschützt. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Zeigt an, ob die`VbaProject` ist signiert oder nicht. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Gibt eine Sammlung von VBA-Projektmodulen zurück. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Ruft den VBA-Projektnamen ab oder legt ihn fest. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Ruft eine Sammlung von VBA-Projektreferenzen ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Führt eine Kopie der`VbaProject` . |

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

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)
