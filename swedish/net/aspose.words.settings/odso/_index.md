---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Settings.Odso för sömlös integrering av dokumentkopplingar. Optimera dina ODSO-inställningar för effektiv hantering av datakällor.
type: docs
weight: 6710
url: /sv/net/aspose.words.settings/odso/
---
## Odso class

Anger ODSO-inställningarna (Office Data Source Object) för en datakälla för dokumentkoppling.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class Odso
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Odso](odso/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Anger det tecken som ska tolkas som kolumnavgränsare som används för att separera kolumner inom externa datakällor. Standardvärdet är 0 vilket innebär att ingen kolumnavgränsare har definierats. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Anger platsen för den externa datakälla som ska anslutas till ett dokument för att utföra dokumentkopplingen. Standardvärdet är en tom sträng. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Anger typen av extern datakälla som ska anslutas till som en del av ODSO-anslutningsinformationen för den här dokumentkopplingen. Standardvärdet ärDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Hämtar eller anger en samling objekt som anger hur kolumner från den externa datakällan mappas till de fördefinierade kopplingsfältnamnen i dokumentet. Detta objekt mappas aldrig`null` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Anger att ett värdprogram ska behandla den första dataraden i den angivna externa data -källan som en rubrikrad som innehåller namnen på varje kolumn i datakällan. Standardvärdet är`falsk` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Hämtar eller anger en samling objekt som anger inkludering/exkludering av enskilda poster i dokumentkopplingen. Detta objekt är aldrig`null` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Anger den specifika datamängd som en källa ska vara kopplad till inom en extern datakälla. Standardvärdet är en tom sträng. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Anger den UDL-anslutningssträng (Universal Data Link) som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Returnerar en djup klon av detta objekt. |

## Anmärkningar

ODSO verkar vara det "nya" sättet som de nyare Microsoft Word-versionerna föredrar att använda när man anger vissa typer av datakällor för ett dokument för koppling av dokument. ODSO dök förmodligen först upp i Microsoft Word 2000.

Användningen av ODSO är dåligt dokumenterad och det bästa sättet att lära sig använda egenskaperna för detta objekt är att manuellt skapa ett dokument med en önskad datakälla i Microsoft Word och sedan öppna det dokumentet med Aspose.Words och undersöka egenskaperna för[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) och [`Odso`](../mailmergesettings/odso/)objekt. Detta är en bra metod att använda om du till exempel vill lära dig hur man programmatiskt konfigurerar en datakälla.

Du behöver normalt inte skapa objekt av den här klassen direkt eftersom ODSO settings alltid är tillgängliga via[`Odso`](../mailmergesettings/odso/) egendom.

## Exempel

Visar hur man utför en dokumentkoppling med data från ett Office-datakällobjekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Skapa en datakälla i form av en ASCII-fil, med tecknet "|"
// fungerar som avgränsare som separerar kolumner. Den första raden innehåller namnen på de tre kolumnerna,
// och varje efterföljande rad är en rad med deras respektive värden.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // Om du öppnar det här dokumentet i Microsoft Word körs dokumentkopplingen innan innehållet visas.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Se även

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
