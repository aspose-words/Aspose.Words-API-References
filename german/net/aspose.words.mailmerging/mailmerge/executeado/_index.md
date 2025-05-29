---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumenterstellung mit der MailMerge ExecuteADO-Methode. Führen Sie mühelos ADO-Recordset-Daten für eine effiziente, personalisierte Ausgabe zusammen.
type: docs
weight: 190
url: /de/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Führt einen Seriendruck von einem ADO-Recordset-Objekt in das Dokument aus.

```csharp
public void ExecuteADO(object recordset)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| recordset | Object | ADO-Recordset oder Record-Objekt. |

## Bemerkungen

Diese Methode ist nützlich, wenn Sie Aspose.Words-Klassen als COM-Objekte aus nicht verwaltetem Code verwenden möchten, z. B. einer mit ASP oder Visual Basic 6.0 erstellten Anwendung.

Diese Methode ignoriert dieRemoveUnusedRegions Option.

Weitere Informationen finden Sie in der Beschreibung von[`Execute`](../execute/).

## Beispiele

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

Zeigt, wie ein Serienbrief mit Daten aus einem ADO-Dataset ausgeführt wird.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Serienbrief ausführen und Dokument speichern.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Erstellen Sie ein leeres Dokument und füllen Sie es mit MERGEFIELDS, die Daten akzeptieren, wenn ein Serienbrief ausgeführt wird.
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

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
