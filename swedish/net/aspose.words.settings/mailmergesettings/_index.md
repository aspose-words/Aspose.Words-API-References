---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.MailMergeSettings för att effektivisera dokumentautomation med kraftfulla funktioner för dokumentkoppling och ökad effektivitet.
type: docs
weight: 6680
url: /sv/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Anger all information om dokumentkoppling för ett dokument.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class MailMergeSettings
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Anger det enbaserade indexet för posten från datakällan som ska visas i Microsoft Word. Standardvärdet är 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Anger kolumnen i datakällan som innehåller e-postadresser. Standardvärdet är en tom sträng. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Anger vilken typ av felrapportering som ska utföras av Microsoft Word vid dokumentkoppling. Standardvärdet ärDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Anger anslutningssträngen som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Anger sökvägen till datakällan för dokumentkopplingen. Standardvärdet är en tom sträng. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Anger typen av datakälla för dokumentkoppling och metoden för dataåtkomst. Standardvärdet ärDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Anger hur Microsoft Word ska skriva ut resultatet av en dokumentkoppling. Standardvärdet ärDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Anger hur ett program som utför dokumentkopplingen ska hantera tomma rader i de sammanfogade dokumenten som är resultatet av dokumentkopplingen. Standardvärdet är`falsk` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Anger sökvägen till källan för headern för koppling av dokument. Standardvärdet är en tom sträng. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Inte säker på den här. Microsoft Word Automation Reference föreslår att detta anger att frågan körs varje gång dokumentet öppnas i Microsoft Word. Men OOXML-specifikationen föreslår att detta anger att frågan innehåller en referens till en extern frågefil som innehåller den faktiska frågan. Standardvärdet är`falsk` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Anger att dokument som skapas under en dokumentkoppling ska skickas via e-post som en bilaga snarare än som brödtexten i själva e-postmeddelandet. Standardvärdet är `falsk` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Anger texten som ska visas i ämnesraden för e-postmeddelanden eller fax som skapas under dokumentkopplingen. Standardvärdet är en tom sträng. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Anger huvuddokumenttypen för dokumentkopplingen. Standardvärdet ärDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Hämtar eller ställer in objektet som anger inställningarna för Office Data Source Object (ODSO). |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Innehåller strängen för Structured Query Language som ska köras mot den angivna externa datakällan för att returnera den uppsättning poster som ska importeras till dokumentet när dokumentkopplingen utförs. Standardvärdet är en tom sträng. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Anger att Microsoft Word ska visa data från den angivna externa datakällan där kopplingsfält har infogats (t.ex. förhandsgranska kopplingsdata). Standardvärdet är`falsk` . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Rensar inställningarna för koppling av dokument på ett sådant sätt att när dokumentet sparas, sparas inga inställningar för koppling av dokument och det blir ett normalt dokument. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Returnerar en djup klon av detta objekt. |

## Anmärkningar

Du kan använda det här objektet för att ange en datakälla för kopplad dokument för ett dokument och denna information (tillsammans med tillgängliga datafält) visas i Microsoft Word när användaren öppnar dokumentet. Eller så kan du använda det här objektet för att fråga efter inställningar för kopplad dokument som användaren har angett i Microsoft Word för det här dokumentet.

Du behöver normalt inte skapa objekt av den här klassen direkt eftersom inställningarna för dokumentkoppling för ett dokument alltid är tillgängliga via[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) egendom.

För att avgöra om det här dokumentet är ett huvuddokument för dokumentkoppling, kontrollera värdet för [`MainDocumentType`](./maindocumenttype/) egendom.

För att ta bort inställningar för dokumentkoppling och datakällinformation från ett dokument kan du använda [`Clear`](./clear/) metod. Aspose.Words skriver inte inställningar för koppling av dokument till ett dokument om [`MainDocumentType`](./maindocumenttype/) egendomen är inställd påNotAMergeDocument eller den[`DataType`](./datatype/) egendomen är inställd påNone.

Det bästa sättet att lära sig använda egenskaperna för det här objektet är att manuellt skapa ett dokument med en önskad -datakälla i Microsoft Word och sedan öppna dokumentet med Aspose.Words och undersöka egenskaperna för den.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) och[`Odso`](./odso/) objekt. Detta är en bra metod att använda om du till exempel vill lära dig hur man programmatiskt konfigurerar en datakälla.

Aspose.Words bevarar information om dokumentkoppling när den laddar, sparar och konverterar dokument mellan olika format, men använder inte denna information när den utför sin egen dokumentkoppling med hjälp av[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) objekt.

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
