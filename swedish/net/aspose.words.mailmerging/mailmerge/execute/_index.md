---
title: Execute
second_title: Aspose.Words för .NET API Referens
description: Utför en epostsammanfogning från en anpassad datakälla.
type: docs
weight: 180
url: /sv/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Utför en e-postsammanfogning från en anpassad datakälla.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ett objekt som implementerar det anpassade gränssnittet för kopplingsdatakällan. |

### Anmärkningar

Använd den här metoden för att fylla sammankopplingsfält i dokumentet med värden from vilken datakälla som helst som en lista eller hashtabell eller objekt. Du måste skriva din egen klass som implementerar[`IMailMergeDataSource`](../../imailmergedatasource/) gränssnitt.

Du kan bara använda den här metoden när[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)är falsk, det vill säga att du inte behöver höger-till-vänster-språk (som arabiska eller hebreiska) kompatibilitet.

Denna metod ignorerarRemoveUnusedRegions alternativ.

### Se även

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Utför en kopplingsoperation för en enskild post.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldNames | String[] | Array av sammanslagningsfältnamn. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| values | Object[] | Matris med värden som ska infogas i sammanslagningsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |

### Anmärkningar

Använd den här metoden för att fylla sammankopplingsfält i dokumentet med värden from en array av objekt.

Denna metod slår samman data för endast en post. Matrisen av fältnamn och matrisen av värden representerar data för en enskild post.

Den här metoden använder inte kopplingsregioner.

Denna metod ignorerarRemoveUnusedRegions alternativ.

### Exempel

Visar hur man slår samman en bild från en URI som e-postsammanfogningsdata till ett MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs med "Image:"-taggar kommer att få en bild under en e-postsammanfogning.
// Strängen efter kolon i taggen "Image:" motsvarar ett kolumnnamn
// i datakällan vars celler innehåller URI:er av bildfiler.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

  // Skapa en datakälla som innehåller URI:er av bilder som vi kommer att slå samman.
// En URI kan vara en webbadress som pekar på en bild, eller ett lokalt filsystems filnamn för en bildfil.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Kör en e-postsammanfogning på en datakälla med en rad.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Visar hur man utför en sammanfogning och sedan sparar dokumentet i klientens webbläsare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Skicka dokumentet till klientens webbläsare.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Kastad eftersom HttpResponse är null i testet.

// Vi kommer att behöva stänga detta svar manuellt för att säkerställa att vi inte lägger till något överflödigt innehåll i dokumentet efter att ha sparats.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Utför e-postkoppling från en datatabell till dokumentet.

```csharp
public void Execute(DataTable table)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| table | DataTable | Tabell som innehåller data som ska infogas i kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |

### Anmärkningar

Använd den här metoden för att fylla sammanslagningsfält i dokumentet med värden från a  **Datatabell**.

Alla poster från tabellen slås samman i dokumentet.

Du kan använda NÄSTA-fältet i Word-dokumentet för att orsaka **MailMerge** objekt för att välja nästa post från **Datatabell** och fortsätt sammanfoga. Detta kan användas när du skapar dokument som adressetiketter.

När **MailMerge**objektet når slutet av huvuddokumentet och det finns fortfarande fler rader i **Datatabell**, kopierar det hela innehållet i huvuddokumentet och lägger till det i slutet av måldokumentet med en section break som avgränsare.

Denna metod ignorerarRemoveUnusedRegions alternativ.

### Exempel

Visar hur man kör en e-postsammanfogning med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan finns två sätt att använda en datatabell som datakälla för en e-postkoppling.
    // 1 - Använd hela tabellen för kopplingen för att skapa ett kopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett dokument för utmatning av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för sammankoppling av brev.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Utför e-postkoppling från IDataReader till dokumentet.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataReader | IDataReader | Datakälla för sammankopplingsåtgärden. |

### Anmärkningar

Du kan passera **SqlDataReader** eller **OleDbDataReader** objekt till denna -metoden som en parameter eftersom de båda implementerade **IDataReader** gränssnitt.

Observera att den här metoden inte använder kopplingsregioner och för flera poster kommer dokumentet att växa genom att hela dokumentet upprepas.

Denna metod ignorerarRemoveUnusedRegions alternativ.

### Exempel

Visar hur man kör en sammankoppling av brev med data från en dataläsare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// Skapa en anslutningssträng som pekar på databasfilen "Northwind".
// i vårt lokala filsystem, öppna en anslutning och ställ in en SQL-fråga.
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // Skapa ett SQL-kommando som kommer att hämta data för vår sammanslagning.
    // Namnen på tabellens kolumner som denna SELECT-sats kommer att returnera
    // kommer att behöva motsvara sammanslagningsfälten vi placerade ovan.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // Detta kommer att köra kommandot och lagra data i läsaren.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Ta data från läsaren och använd den i kopplingen.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Utför e-postkoppling från en DataView till dokumentet.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataView | DataView | Datakälla för sammankopplingsåtgärden. |

### Anmärkningar

Den här metoden är användbar om du hämtar data till en **Datatabell** men då måste tillämpa ett filter eller sortera innan sammanslagningen.

Observera att den här metoden inte använder kopplingsregioner och för flera poster kommer dokumentet att växa genom att hela dokumentet upprepas.

Denna metod ignorerarRemoveUnusedRegions alternativ.

### Exempel

Visar hur man redigerar sammanslagningsdata med en DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Skapa en datatabell som vår sammanslagning kommer att hämta data från.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Vi kan använda en datavy för att ändra kopplingsdata utan att göra ändringar i själva datatabellen.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Vår datavy sorterar posterna i fallande ordning längs kolumnen "Betyg".
// och filtrerar bort rader med värden mindre än 50 i den kolumnen.
// Tre av de fyra raderna passar dessa kriterier så att utdatadokumentet kommer att innehålla tre sammanslagningsdokument.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Utför e-postkoppling från en DataRow till dokumentet.

```csharp
public void Execute(DataRow row)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| row | DataRow | Rad som innehåller data som ska infogas i kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |

### Anmärkningar

Använd den här metoden för att fylla sammankopplingsfält i dokumentet med värden från a **DataRow**.

Denna metod ignorerarRemoveUnusedRegions alternativ.

### Exempel

Visar hur man kör en e-postsammanfogning med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan finns två sätt att använda en datatabell som datakälla för en e-postkoppling.
    // 1 - Använd hela tabellen för kopplingen för att skapa ett kopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett dokument för utmatning av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för sammankoppling av brev.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
