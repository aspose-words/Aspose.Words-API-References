---
title: Class JsonDataLoadOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Reporting.JsonDataLoadOptions klass. Representerar alternativ för att analysera JSONdata.
type: docs
weight: 4680
url: /sv/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Representerar alternativ för att analysera JSON-data.

För att lära dig mer, besök[LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class JsonDataLoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Initierar en ny instans av denna klass med standardalternativ. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Hämtar eller ställer in en flagga som indikerar om en genererad datakälla alltid kommer att innehålla ett objekt för ett JSON root element. Om ett JSON-rotelement innehåller en enda komplex egenskap skapas inte ett sådant objekt som standard. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Hämtar eller ställer in exakta format för att analysera JSON-datum-tid-värden när JSON laddas. Standard är`null` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Hämtar eller ställer in en flagga som indikerar om inledande och efterföljande mellanslag ska bevaras när string värden för JSON-data laddas. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Hämtar eller ställer in ett läge för att analysera JSON enkla värden (null, boolean, nummer, heltal och sträng) medan JSON laddas. Ett sådant läge påverkar inte analysen av datum-tid-värden. Standard är Loose . |

### Anmärkningar

En instans av denna klass kan skickas till konstruktörer av[`JsonDataSource`](../jsondatasource/) .

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)


