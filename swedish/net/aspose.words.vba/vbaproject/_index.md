---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words för .NET
description: Lås upp kraften i Aspose.Words.Vba.VbaProject-klassen för att enkelt hantera VBA-projektinformation och moduler i dina dokument. Förbättra din automatisering idag!
type: docs
weight: 7430
url: /sv/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Ger åtkomst till VBA-projektinformation. Ett VBA-projekt inuti dokumentet definieras som en samling VBA-moduler.

För att lära dig mer, besök[Arbeta med VBA-makron](https://docs.aspose.com/words/net/working-with-vba-macros/) dokumentationsartikel.

```csharp
public class VbaProject
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [VbaProject](vbaproject/)() | Skapar ett tomrum`VbaProject` . |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Hämtar eller ställer in VBA-projektets kodsida. |
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | Visar om`VbaProject` är lösenordsskyddad. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Visar om`VbaProject` är signerad eller inte. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Returnerar en samling av VBA-projektmoduler. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Hämtar eller anger VBA-projektnamn. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Hämtar en samling VBA-projektreferenser. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Utför en kopia av`VbaProject` . |

## Exempel

Visar hur man kommer åt ett dokuments VBA-projektinformation.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Ett VBA-projekt innehåller en samling VBA-moduler.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules;

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Ange ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen via index eller namn.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Ta bort en modul från samlingen.
vbaModules.Remove(vbaModules[2]);
```

### Se även

* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)
