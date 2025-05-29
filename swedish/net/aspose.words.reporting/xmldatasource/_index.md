---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words för .NET
description: Lås upp kraftfull rapportering med Aspose.Words.XmlDataSource. Få enkel åtkomst till XML-data för sömlös integration i dina rapporter och förbättra datavisualiseringen.
type: docs
weight: 5490
url: /sv/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Ger åtkomst till data från en XML-fil eller ström som ska användas i en rapport.

För att lära dig mer, besök[LINQ-rapporteringsmotor](https://docs.aspose.com/words/net/linq-reporting-engine/) dokumentationsartikel.

```csharp
public class XmlDataSource
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Skapar en ny datakälla med data från en XML-ström med standardalternativ för inläsning av XML-data. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Skapar en ny datakälla med data från en XML-fil med standardalternativ för inläsning av XML-data. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Skapar en ny datakälla med data från en XML-ström med hjälp av en XML Schema Definition-ström. Standardalternativen används för inläsning av XML-data. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-ström med hjälp av de angivna alternativen för XML-datainläsning. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Skapar en ny datakälla med data från en XML-fil med hjälp av en XML-schemadefinitionsfil. Standardalternativen används för inläsning av XML-data. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-fil med hjälp av de angivna alternativen för inläsning av XML-data. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-ström med hjälp av en XML Schema Definition-ström. De angivna -alternativen används för inläsning av XML-data. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Skapar en ny datakälla med data från en XML-fil med hjälp av en XML-schemadefinitionsfil. De angivna -alternativen används för inläsning av XML-data. |

## Anmärkningar

För att komma åt data i motsvarande fil eller ström när du genererar en rapport, skicka en instans av denna klass som en datakälla till en av[`ReportingEngine`](../reportingengine/) .BuildReport överbelastningar.

Om ett XML-element på översta nivån i malldokument bara innehåller en lista med element av samma typ, `XmlDataSource` instansen bör behandlas på samma sätt som om den vore aDataTable -instans. Annars en`XmlDataSource` instansen bör behandlas på samma sätt som om den vore aDataRow -instansen. För mer information, se mallsyntaxreferensen (https://docs.aspose.com/display/wordsnet/Template+Syntax).

När XML-schemadefinitionen skickas till en konstruktor av den här klassen bestäms datatyper för värden för enkla XML-element och attribut enligt schemat. Så i malldokument kan du arbeta med typade värden snarare än bara strängar.

När XML-schemadefinitionen inte skickas till en konstruktor av den här klassen, bestäms datatyper för värden i enkla XML-element och attribut automatiskt utifrån deras strängrepresentationer. Så i malldokument kan du arbeta med typskrivna värden även i det här fallet. Motorn kan automatiskt känna igen värden av följande typer:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Observera att för att automatisk igenkänning av datatyper ska fungera bör strängrepresentationer av värden för enkla XML-element och attribut bildas med hjälp av invarianta kulturinställningar.

För att åsidosätta standardbeteendet för XML-datainläsning, initiera och skicka en[`XmlDataLoadOptions`](../xmldataloadoptions/) -instansen till en konstruktor av den här klassen.

## Exempel

Visa hur man använder XML som datakälla (sträng).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

Visa hur man använder XML som datakälla (ström).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)
