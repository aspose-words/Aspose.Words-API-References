---
title: MailMerge.ExecuteWithRegionsADO
second_title: Aspose.Words för .NET API Referens
description: MailMerge metod. Utför koppling från ett ADO Recordsetobjekt till dokumentet med kopplingsregioner.
type: docs
weight: 210
url: /sv/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Utför koppling från ett ADO Recordset-objekt till dokumentet med kopplingsregioner.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| recordset | Object | ADO Recordset eller Record-objekt. |
| tableName | String | Namn på kopplingsregionen i dokumentet som ska fyllas i. |

### Anmärkningar

Den här metoden är användbar när du tänker använda Aspose.Words-klasserna as COM-objekt från ohanterad kod, till exempel ett program byggt med ASP eller Visual Basic 6.0.

För mer information se beskrivning av[`ExecuteWithRegions`](../executewithregions/).

### Exempel

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

Visar hur man kör en sammanslagning med flera regioner, sammanställd med data från en ADO-datauppsättning.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // För att arbeta med ADO DataSets måste vi lägga till en referens till Microsoft ActiveX Data Objects-biblioteket,
    // som ingår i .NET-distributionen och lagras i "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Skapa en anslutningssträng som pekar på databasfilen "Northwind".
    // i vårt lokala filsystem och öppna en anslutning.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Fyll i vår datauppsättning genom att köra ett SQL-kommando på vår databas.
    // Namnen på kolumnerna i resultattabellen måste överensstämma
    // till värdena för MERGEFIELDS som kommer att rymma våra data.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Kör en e-postkoppling på bara den första regionen, fyll dess MERGEFIELDS med data från postuppsättningen.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Stäng postuppsättningen och öppna den igen med data från en annan SQL-fråga.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Kör en andra sammanfogning på den andra regionen och spara dokumentet.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// Skapa ett dokument med två kopplingsregioner.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)


