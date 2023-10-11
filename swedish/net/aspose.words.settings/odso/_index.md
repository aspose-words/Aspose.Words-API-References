---
title: Class Odso
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.Odso klass. Anger ODSOinställningarna Office Data Source Object för en kopplingsdatakälla.
type: docs
weight: 5880
url: /sv/net/aspose.words.settings/odso/
---
## Odso class

Anger ODSO-inställningarna (Office Data Source Object) för en kopplingsdatakälla.

För att lära dig mer, besök[Mail Merge och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

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
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Anger tecknet som ska tolkas som kolumnavgränsaren som används för att separera kolumner inom externa datakällor. Standardvärdet är 0 vilket betyder att det inte finns någon kolumnavgränsare definierad. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Anger platsen för den externa datakällan som ska anslutas till ett dokument för att utföra kopplingen. Standardvärdet är en tom sträng. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Anger typen av den externa datakällan som ska anslutas till som en del av ODSO-anslutningsinformationen för denna koppling. Standardvärdet ärDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Hämtar eller ställer in en samling objekt som anger hur kolumner från den externa datakällan mappas till de fördefinierade sammanslagningsfältsnamnen i dokumentet. Detta objekt är aldrig`null` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Anger att en värdapplikation ska behandla den första raden med data i den angivna externa data -källan som en rubrikrad som innehåller namnen på varje kolumn i datakällan. Standardvärdet är`falsk` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Hämtar eller ställer in en samling objekt som anger inkludering/exkludering av enskilda poster i kopplingen. Detta objekt är aldrig`null` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Anger den särskilda uppsättning data som en källa ska anslutas till inom en extern datakälla. Standardvärdet är en tom sträng. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Anger anslutningssträngen Universal Data Link (UDL) som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Returnerar en djup klon av detta objekt. |

### Anmärkningar

ODSO verkar vara det "nya" sättet som de nyare Microsoft Word-versionerna föredrar att använda när de specificerar vissa -typer av datakällor för ett kopplingsdokument. ODSO dök förmodligen först upp i Microsoft Word 2000.

Användningen av ODSO är dåligt dokumenterad och det bästa sättet att lära sig hur man använder egenskaperna för detta objekt är att skapa ett dokument med en önskad datakälla manuellt i Microsoft Word och sedan öppna det dokumentet med Aspose.Words och undersöka egenskaperna av[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) och [`Odso`](../mailmergesettings/odso/)föremål. Det här är ett bra tillvägagångssätt om du vill lära dig hur du programmatiskt konfigurerar en datakälla, till exempel.

Du behöver normalt inte skapa objekt av denna klass direkt eftersom ODSO settings alltid är tillgängliga via[`Odso`](../mailmergesettings/odso/) fast egendom.

### Exempel

Visar hur man kör en sammankoppling med data från ett Office-datakällobjekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Skapa en datakälla i form av en ASCII-fil, med "|" karaktär
// fungerar som avgränsaren som separerar kolumner. Den första raden innehåller de tre kolumnernas namn,
// och varje efterföljande rad är en rad med sina respektive värden.
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

 // Att öppna detta dokument i Microsoft Word kommer att köra sammanslagningen innan innehållet visas.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Se även

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


