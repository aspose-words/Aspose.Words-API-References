---
title: MailMergeSettings
second_title: Aspose.Words för .NET API Referens
description: Anger all kopplingsinformation för ett dokument.
type: docs
weight: 5550
url: /sv/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Anger all kopplingsinformation för ett dokument.

```csharp
public class MailMergeSettings
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MailMergeSettings](mailmergesettings)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord) { get; set; } | Anger det enbaserade indexet för posten från datakällan som ska visas i Microsoft Word. Standardvärdet är 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname) { get; set; } | Anger kolumnen i datakällan som innehåller e-postadresser. Standardvärdet är en tom sträng. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors) { get; set; } | Anger vilken typ av felrapportering som ska utföras av Microsoft Word när en sammankoppling av e-post utförs. Standardvärdet ärDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring) { get; set; } | Anger anslutningssträngen som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource) { get; set; } | Anger sökvägen till kopplingsdatakällan. Standardvärdet är en tom sträng. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype) { get; set; } | Anger typen av kopplingsdatakällan och metoden för dataåtkomst. Standardvärdet ärDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination) { get; set; } | Anger hur Microsoft Word kommer att mata ut resultaten av en e-postsammanfogning. Standardvärdet ärDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines) { get; set; } | Anger hur ett program som utför kopplingen ska hantera tomma rader i de sammanslagna dokumenten som är resultatet av kopplingen. Standardvärdet är`falsk` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource) { get; set; } | Anger sökvägen till källan för kopplingshuvudet. Standardvärdet är en tom sträng. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery) { get; set; } | Inte säker på den här. Microsoft Word Automation Reference föreslår att denna anger att frågan exekveras varje gång dokumentet öppnas i Microsoft Word. Men OOXML-specifikationen antyder att denna anger att frågan innehåller en referens till en extern frågefil som innehåller den faktiska frågan. Standardvärdet är`falsk` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment) { get; set; } | Anger att dokumenten som skapas under en sammankopplingsåtgärd ska skickas som en bilaga via e-post snarare än själva e-postmeddelandets brödtext. Standardvärdet är`falsk` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject) { get; set; } | Anger texten som ska visas i ämnesraden för e-postmeddelanden eller fax som produceras under sammanslagningen. Standardvärdet är en tom sträng. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype) { get; set; } | Anger huvuddokumenttypen för sammankoppling. Standardvärdet ärDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso) { get; set; } | Hämtar eller ställer in objektet som anger ODSO-inställningarna (Office Data Source Object). |
| [Query](../../aspose.words.settings/mailmergesettings/query) { get; set; } | Innehåller Structured Query Language-strängen som ska köras mot den angivna externa datakällan för att returnera den uppsättning poster som ska importeras till dokumentet när kopplingsoperationen utförs. Standardvärdet är en tom sträng. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata) { get; set; } | Anger att Microsoft Word ska visa data från den angivna externa datakällan där sammanslagningsfälten har infogats (t.ex. förhandsgranska sammanslagna data). Standardvärdet är`falsk` . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear)() | Rensar inställningarna för sammankoppling av dokument på ett sådant sätt att när dokumentet sparas, kommer inga sammanslagningsinställningar att sparas och det blir ett normalt dokument. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone)() | Returnerar en djup klon av detta objekt. |

### Anmärkningar

Du kan använda det här objektet för att ange en kopplingsdatakälla för ett dokument och denna information (tillsammans med de tillgängliga datafälten) kommer att visas i Microsoft Word när användaren öppnar det här dokumentet. Eller så kan du använda det här objektet för att fråga inställningar för koppling av e-post som användaren har angett i Microsoft Word för detta dokument.

Du behöver normalt inte skapa objekt av den här klassen direkt eftersom inställningar för koppling av dokument för ett dokument alltid är tillgängliga via[`MailMergeSettings`](../../aspose.words/document/mailmergesettings) fast egendom.

För att upptäcka om det här dokumentet är ett huvuddokument för sammankoppling av e-post, kontrollera värdet på [`MainDocumentType`](./maindocumenttype) fast egendom.

För att ta bort sammanslagningsinställningar och datakällainformation från ett dokument kan du använda [`Clear`](./clear) metod. Aspose.Words kommer inte att skriva sammanslagningsinställningar till ett dokument om [`MainDocumentType`](./maindocumenttype) egenskapen är inställd påNotAMergeDocument eller[`DataType`](./datatype) egenskapen är inställd påNone.

Det bästa sättet att lära sig hur man använder egenskaperna för detta objekt är att skapa ett dokument med en önskad -datakälla manuellt i Microsoft Word och sedan öppna det dokumentet med Aspose.Words och undersöka egenskaperna för[`MailMergeSettings`](../../aspose.words/document/mailmergesettings) och[`Odso`](./odso) objekt. Det här är ett bra tillvägagångssätt om du till exempel vill lära dig hur du programmatiskt konfigurerar en datakälla.

Aspose.Words bevarar kopplingsinformation när du laddar, sparar och konverterar documents mellan olika format, men använder inte denna information när du utför sin egen kopplingsinformation med hjälp av[`MailMerge`](../../aspose.words.mailmerging/mailmerge) objekt.

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

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
