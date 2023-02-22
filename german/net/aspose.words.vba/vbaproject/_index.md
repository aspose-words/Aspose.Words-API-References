---
title: Class VbaProject
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Vba.VbaProject klas. Bietet Zugriff auf VBAProjektinformationen. Ein VBAProjekt innerhalb des Dokuments ist als Sammlung von VBAModulen definiert.
type: docs
weight: 6270
url: /de/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Bietet Zugriff auf VBA-Projektinformationen. Ein VBA-Projekt innerhalb des Dokuments ist als Sammlung von VBA-Modulen definiert.

```csharp
public class VbaProject
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [VbaProject](vbaproject/)() | Erstellt ein leeres VbaProject. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; } | Gibt die Codepage des VBA-Projekts zurück. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Zeigt an, ob das VbaProject signiert ist oder nicht. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Gibt eine Sammlung von VBA-Projektmodulen zurück. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Ruft den VBA-Projektnamen ab oder legt ihn fest. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Ruft eine Sammlung von VBA-Projektreferenzen ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Führt eine Kopie der`VbaProject` . |

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

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)


