---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Vba.VbaModuleType, som definierar modelltyper i VBA-projekt för förbättrad automatisering och effektiv dokumenthantering.
type: docs
weight: 7420
url: /sv/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Anger typen av en modell i ett VBA-projekt.

```csharp
public enum VbaModuleType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| DocumentModule | `0` | En typ av VBA-projektobjekt som anger en modul för inbäddade makron och programmatiska åtkomståtgärder som är associerade med ett dokument. |
| ProceduralModule | `1` | En samling subrutiner och funktioner. |
| ClassModule | `2` | En modul som innehåller definitionen för ett nytt objekt. Varje instans av en klass skapar ett nytt objekt, och procedurer som definieras i modulen blir egenskaper och metoder för objektet. |
| DesignerModule | `3` | En VBA-modul som utökar metoderna och egenskaperna för en ActiveX-kontroll som har registrerats med projektet. |

## Exempel

Visar hur man skapar ett VBA-projekt med hjälp av makron.

```csharp
Document doc = new Document();

// Skapa ett nytt VBA-projekt.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Skapa en ny modul och ange en makrokällkod.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Lägg till modulen i VBA-projektet.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Se även

* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)
