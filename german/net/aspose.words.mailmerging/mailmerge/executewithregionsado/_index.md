---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumenterstellung mit der MailMerge ExecuteWithRegionsADO-Methode. Führen Sie mühelos ADO-Recordset-Daten zusammen, um personalisierte Ergebnisse zu erzielen.
type: docs
weight: 210
url: /de/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Führt einen Seriendruck von einem ADO-Recordset-Objekt in das Dokument mit Seriendruckbereichen durch.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| recordset | Object | ADO-Recordset oder Record-Objekt. |
| tableName | String | Name des Serienbriefbereichs im Dokument, der ausgefüllt werden soll. |

## Bemerkungen

Diese Methode ist nützlich, wenn Sie Aspose.Words-Klassen als COM-Objekte aus nicht verwaltetem Code verwenden möchten, z. B. einer mit ASP oder Visual Basic 6.0 erstellten Anwendung.

Weitere Informationen finden Sie in der Beschreibung von[`ExecuteWithRegions`](../executewithregions/).

## Beispiele

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

Zeigt, wie ein Serienbrief mit mehreren Regionen ausgeführt wird, der mit Daten aus einem ADO-Dataset kompiliert wurde.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // Um mit ADO-DataSets zu arbeiten, müssen wir einen Verweis auf die Microsoft ActiveX Data Objects-Bibliothek hinzufügen.
    // das in der .NET-Distribution enthalten und in „adodb.dll“ gespeichert ist.
    ADODB.Connection connection = new ADODB.Connection();

    // Erstellen Sie eine Verbindungszeichenfolge, die auf die Datenbankdatei „Northwind“ verweist
    // in unserem lokalen Dateisystem und öffnen Sie eine Verbindung.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Füllen Sie unseren Datensatz, indem Sie einen SQL-Befehl in unserer Datenbank ausführen.
    // Die Namen der Spalten in der Ergebnistabelle müssen übereinstimmen
    // auf die Werte der MERGEFIELDS, die unsere Daten aufnehmen.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Führen Sie einen Serienbrief nur für die erste Region aus und füllen Sie deren MERGEFIELDS mit Daten aus dem Datensatz.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Schließen Sie den Datensatz und öffnen Sie ihn erneut mit Daten aus einer anderen SQL-Abfrage.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Führen Sie einen zweiten Serienbrief für die zweite Region aus und speichern Sie das Dokument.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// Erstellen Sie ein Dokument mit zwei Serienbriefbereichen.
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

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
