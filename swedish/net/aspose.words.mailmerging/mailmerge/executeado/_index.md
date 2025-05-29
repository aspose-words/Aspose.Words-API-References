---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words för .NET
description: Effektivisera ditt dokumentskapande med MailMerge ExecuteADO-metoden. Sammanfoga enkelt ADO Recordset-data för effektiv och personlig utskrift.
type: docs
weight: 190
url: /sv/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Utför dokumentkoppling från ett ADO Recordset-objekt till dokumentet.

```csharp
public void ExecuteADO(object recordset)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| recordset | Object | ADO-postuppsättning eller postobjekt. |

## Anmärkningar

Den här metoden är användbar när du tänker använda Aspose.Words-klasser som COM-objekt från ohanterad kod, till exempel ett program som byggts med ASP eller Visual Basic 6.0.

Denna metod ignorerarRemoveUnusedRegions alternativ.

För mer information se beskrivningen av[`Execute`](../execute/).

## Exempel

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

Visar hur man kör en dokumentkoppling med data från en ADO-datauppsättning.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

    // För att arbeta med ADO DataSets måste vi lägga till en referens till Microsoft ActiveX Data Objects-biblioteket,
    // som ingår i .NET-distributionen och lagras i "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Skapa en anslutningssträng som pekar till databasfilen "Northwind"
    // i vårt lokala filsystem och öppna en anslutning.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Fyll i vår dataset genom att köra ett SQL-kommando i vår databas.
    // Namnen på kolumnerna i resultattabellen måste överensstämma
    // till värdena för MERGEFIELDS som kommer att rymma våra data.
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Kör dokumentkopplingen och spara dokumentet.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Skapa ett tomt dokument och fyll det med MERGEFIELDS som accepterar data när en dokumentkoppling körs.
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
