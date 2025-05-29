---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words för .NET
description: Lås upp kraftfull dokumentautomation med Aspose.Words.ReportingEngine. Fyll enkelt i mallar med data och anpassa inställningar för sömlös rapportering.
type: docs
weight: 5470
url: /sv/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Tillhandahåller rutiner för att fylla malldokument med data och en uppsättning inställningar för att styra dessa rutiner.

För att lära dig mer, besök[LINQ-rapporteringsmotor](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class ReportingEngine
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Hämtar en oordnad mängd (dvs. en samling unika objekt) som innehållerType objekt vars helt eller delvis kvalificerade namn kan användas inom rapportmallar som bearbetas av denna engine -instans för att anropa motsvarande typers statiska medlemmar, utföra typomvandlingar etc. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Hämtar eller ställer in ett strängvärde som skrivs ut istället för ett malluttryck som representerar en vanlig referens till en saknad medlem i ett objekt. Standardvärdet är en tom sträng. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Hämtar eller ställer in en uppsättning flaggor som styr beteendet hos detta`ReportingEngine` instans när du skapar en rapport. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Hämtar eller ställer in ett värde som anger om anrop av anpassade typmedlemmar som utförs via reflektions-API är optimerade med dynamisk klassgenerering eller inte. Standardvärdet är`sann` . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Fyller det angivna malldokumentet med data från den angivna källan, vilket gör det till en färdig rapport. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Fyller det angivna malldokumentet med data från den angivna källan, vilket gör det till en färdig rapport. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Fyller det angivna malldokumentet med data från de angivna källorna, vilket gör det till en färdig rapport. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Returnerar typer, vilka medlemmar samt vilka härledda typers medlemmar ska vara oåtkomliga för motorn. via mallsyntaxen. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Anger typer, vilka medlemmar samt vilka härledda typers medlemmar som ska vara oåtkomliga för motorn. via mallsyntaxen. |

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
