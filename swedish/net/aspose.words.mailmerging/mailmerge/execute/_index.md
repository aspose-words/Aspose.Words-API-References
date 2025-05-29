---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words för .NET
description: Effektivisera din utskicksprocess med MailMerge Execute-metoden, och sammanfoga enkelt data från anpassade källor för personlig kommunikation.
type: docs
weight: 180
url: /sv/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Utför en dokumentkoppling från en anpassad datakälla.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ett objekt som implementerar det anpassade gränssnittet för datakällan för dokumentkoppling. |

## Anmärkningar

Använd den här metoden för att fylla fält för koppling av dokument i dokumentet med värden från valfri datakälla, till exempel en lista, hashtabell eller objekt. Du måste skriva din egen klass som implementerar[`IMailMergeDataSource`](../../imailmergedatasource/) gränssnitt.

Du kan bara använda den här metoden när[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) är`falsk`, det vill säga, du behöver inte kompatibilitet med höger-till-vänster-språk (som arabiska eller hebreiska).

Denna metod ignorerarRemoveUnusedRegions alternativ.

## Exempel

Visar hur man utför en dokumentkoppling med en datakälla i form av ett anpassat objekt.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // För att använda ett anpassat objekt som datakälla måste det implementera IMailMergeDataSource-gränssnittet.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Ett exempel på en "data entity"-klass i din applikation.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// En anpassad datakälla för dokumentkoppling som du implementerar för att tillåta Aspose.Words
/// för att koppla data från dina kundobjekt till Microsoft Word-dokument.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // När vi initierar datakällan måste dess position vara före den första posten.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Namnet på datakällan. Används endast av Aspose.Words vid dokumentkoppling med repeterbara regioner.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words anropar den här metoden för att hämta ett värde för varje datafält.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            default:
                // Returnera "false" till Aspose.Words-kopplingsmotorn för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// En standardimplementering för att gå till nästa post i en samling.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### Se även

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| values | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i*fieldNames*. |

## Anmärkningar

Använd den här metoden för att fylla fält för koppling av dokument i dokumentet med värden från en array av objekt.

Den här metoden sammanfogar data för endast en post. Matrisen med fältnamn och matrisen med värden representerar data för en enda post.

Den här metoden använder inte områden för dokumentkoppling.

Denna metod ignorerarRemoveUnusedRegions alternativ.

## Exempel

Visar hur man sammanfogar en bild från en URI som dokumentkopplingsdata till ett MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDS med taggarna "Image:" kommer att få en bild under en dokumentkoppling.
// Strängen efter kolon i taggen "Image:" motsvarar ett kolumnnamn
// i datakällan vars celler innehåller URI:er för bildfiler.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Skapa en datakälla som innehåller URI:er för bilder som vi ska sammanfoga.
// En URI kan vara en webb-URL som pekar på en bild, eller ett lokalt filsystemnamn för en bildfil.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Kör en dokumentkoppling på en datakälla med en rad.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Visar hur man utför en dokumentkoppling och sedan sparar dokumentet i klientens webbläsare.

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
//Kastas eftersom HttpResponse är null i testet.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Vi måste stänga detta svar manuellt för att säkerställa att vi inte lägger till något överflödigt innehåll i dokumentet efter att det har sparats.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Utför koppling av dokument från en datatabell till dokumentet.

```csharp
public void Execute(DataTable table)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| table | DataTable | Tabell som innehåller data som ska infogas i fält för dokumentkoppling. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |

## Anmärkningar

Använd den här metoden för att fylla fält för koppling av dokument i dokumentet med värden från a **Datatabell**.

Alla poster från tabellen slås samman i dokumentet.

Du kan använda fältet NEXT i Word-dokumentet för att orsaka[`MailMerge`](../) objekt till select nästa post från**Datatabell** och fortsätt sammanfoga. Detta kan användas när du skapar dokument som adressetiketter.

När[`MailMerge`](../) objektet når slutet av huvuddokumentet och det finns fortfarande fler rader i**Datatabell**kopierar den hela innehållet i huvuddokumentet och lägger till det i slutet av destinationsdokumentet med hjälp av en section -brytning som avgränsare.

Denna metod ignorerarRemoveUnusedRegions alternativ.

## Exempel

Visar hur man utför en dokumentkoppling med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan följer två sätt att använda en datatabell som datakälla för en dokumentkoppling.
    // 1 - Använd hela tabellen för dokumentkopplingen för att skapa ett utgående dokumentkopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett enda dokument för koppling av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för dokumentkoppling.
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
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Utför koppling av dokument från**IDataläsare** in i dokumentet.

```csharp
public void Execute(IDataReader dataReader)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataReader | IDataReader | Datakälla för dokumentkopplingsåtgärden. |

## Anmärkningar

Du kan passera**SqlDataReader** eller**OleDbDataReader**objekt i this -metoden som parameter eftersom båda implementerade**IDataläsare** gränssnitt.

Observera att den här metoden inte använder områden för dokumentkoppling och för flera poster kommer dokumentet att växa genom att upprepa hela dokumentet.

Denna metod ignorerarRemoveUnusedRegions alternativ.

## Exempel

Visar hur man kör en dokumentkoppling med hjälp av data från en dataläsare.

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

// Skapa en anslutningssträng som pekar till databasfilen "Northwind"
// i vårt lokala filsystem, öppna en anslutning och konfigurera en SQL-fråga.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Skapa ett SQL-kommando som ska hämta data för vår koppling av dokument.
    // Namnen på tabellens kolumner som denna SELECT-sats returnerar
    // måste motsvara kopplingsfälten vi placerade ovan.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Ta data från läsaren och använd dem i dokumentkopplingen.
            doc.MailMerge.Execute(reader);
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Utför koppling av dokument från en**Datavy** in i dokumentet.

```csharp
public void Execute(DataView dataView)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataView | DataView | Datakälla för dokumentkopplingsåtgärden. |

## Anmärkningar

Den här metoden är användbar om du hämtar data till en**Datatabell** men sedan behöver du tillämpa ett filter eller en sortering innan dokumentkopplingen.

Observera att den här metoden inte använder områden för dokumentkoppling och för flera poster kommer dokumentet att växa genom att upprepa hela dokumentet.

Denna metod ignorerarRemoveUnusedRegions alternativ.

## Exempel

Visar hur man redigerar dokumentkopplingsdata med en DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Skapa en datatabell som vår dokumentkoppling ska hämta data från.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Vi kan använda en datavy för att ändra dokumentkopplingsdata utan att göra ändringar i själva datatabellen.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Vår datavy sorterar posterna i fallande ordning längs kolumnen "Betyg"
// och filtrerar bort rader med värden mindre än 50 i den kolumnen.
// Tre av de fyra raderna uppfyller dessa kriterier så att utdatadokumentet kommer att innehålla tre sammanslagningsdokument.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Utför koppling av dokument från en**DataRod** in i dokumentet.

```csharp
public void Execute(DataRow row)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| row | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |

## Anmärkningar

Använd den här metoden för att fylla fält för koppling av dokument i dokumentet med värden från en**DataRod**.

Denna metod ignorerarRemoveUnusedRegions alternativ.

## Exempel

Visar hur man utför en dokumentkoppling med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan följer två sätt att använda en datatabell som datakälla för en dokumentkoppling.
    // 1 - Använd hela tabellen för dokumentkopplingen för att skapa ett utgående dokumentkopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett enda dokument för koppling av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för dokumentkoppling.
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
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
