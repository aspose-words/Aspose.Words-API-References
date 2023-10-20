---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words för .NET
description: Aspose.Words.Reporting.XmlDataSource klass. Ger tillgång till data från en XMLfil eller ström som ska användas i en rapport i C#.
type: docs
weight: 4750
url: /sv/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Ger tillgång till data från en XML-fil eller ström som ska användas i en rapport.

För att lära dig mer, besök[LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class XmlDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Skapar en ny datakälla med data från en XML-ström med standardalternativ för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Skapar en ny datakälla med data från en XML-fil med standardalternativ för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Skapar en ny datakälla med data från en XML-ström med hjälp av en XML Schema Definition-ström. Standard options används för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-ström med de angivna alternativen för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Skapar en ny datakälla med data från en XML-fil med hjälp av en XML Schema Definition-fil. Standard options används för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-fil med de angivna alternativen för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-ström med hjälp av en XML Schema Definition-ström. De specificerade -alternativen används för XML-dataladdning. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-fil med hjälp av en XML Schema Definition-fil. De specificerade -alternativen används för XML-dataladdning. |

## Anmärkningar

För att komma åt data för motsvarande fil eller ström medan du genererar en rapport, skicka en instans av den här klassen as en datakälla till en av[`ReportingEngine`](../reportingengine/) .BuildReport overloads.

I malldokument, om ett XML-element på toppnivå endast innehåller en lista med element av samma typ, en`XmlDataSource` instans bör behandlas på samma sätt som om det vore aDataTable instans. Annars, en`XmlDataSource` instans bör behandlas på samma sätt som om det vore aDataRow instans. För mer information, se mallsyntaxreferens (https://docs.aspose.com/display/wordsnet/Template+Syntax).

När XML Schema Definition skickas till en konstruktor av denna klass, bestäms datatyper av värden för enkla XML-element och attribut enligt schemat. Så i malldokument kan du arbeta med inskrivna värden snarare än bara strängar.

När XML Schema Definition inte skickas till en konstruktor av denna klass, bestäms datatyper av värden för enkla XML-element och attribut automatiskt efter deras strängrepresentationer. Så i malldokument kan du arbeta med inskrivna värden också i det här fallet. Motorn kan automatiskt känna igen värden av följande typer:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Observera att för att automatisk igenkänning av datatyper ska fungera bör strängrepresentationer av värden för enkla XML-element och attribut skapas med invarianta kulturinställningar.

För att åsidosätta standardbeteendet för XML-dataladdning, initiera och skicka ett[`XmlDataLoadOptions`](../xmldataloadoptions/) instans till en konstruktor av denna klass.

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
