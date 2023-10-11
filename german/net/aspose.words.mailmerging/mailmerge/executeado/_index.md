---
title: MailMerge.ExecuteADO
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge methode. Führt einen Serienbrief von einem ADORecordsetObjekt in das Dokument durch.
type: docs
weight: 190
url: /de/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Führt einen Serienbrief von einem ADO-Recordset-Objekt in das Dokument durch.

```csharp
public void ExecuteADO(object recordset)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| recordset | Object | ADO-Recordset oder Record-Objekt. |

### Bemerkungen

Diese Methode ist nützlich, wenn Sie Aspose.Words-Klassen als COM-Objekte aus nicht verwaltetem Code verwenden möchten, z. B. einer Anwendung, die mit ASP oder Visual Basic 6.0 erstellt wurde.

Diese Methode ignoriert dieRemoveUnusedRegions Möglichkeit.

Weitere Informationen finden Sie in der Beschreibung von[`Execute`](../execute/).

### Beispiele

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

Zeigt, wie ein Serienbrief mit Daten aus einem ADO-Datensatz ausgeführt wird.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

    // Um mit ADO DataSets arbeiten zu können, müssen wir einen Verweis auf die Microsoft ActiveX Data Objects-Bibliothek hinzufügen.
    // welches in der .NET-Distribution enthalten und in „adodb.dll“ gespeichert ist.
    ADODB.Connection connection = new ADODB.Connection();

    // Erstellen Sie eine Verbindungszeichenfolge, die auf die Datenbankdatei „Northwind“ verweist
    // in unserem lokalen Dateisystem und öffnen Sie eine Verbindung.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Füllen Sie unser DataSet, indem Sie einen SQL-Befehl in unserer Datenbank ausführen.
    // Die Namen der Spalten in der Ergebnistabelle müssen übereinstimmen
    // zu den Werten der MERGEFIELDS, die unsere Daten aufnehmen.
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Führen Sie den Serienbrief aus und speichern Sie das Dokument.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Erstellen Sie ein leeres Dokument und füllen Sie es mit MERGEFIELDS, das Daten akzeptiert, wenn ein Serienbrief ausgeführt wird.
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
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)


