---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words per .NET
description: MailMerge ExecuteADO metodo. Esegue la stampa unione da un oggetto ADO Recordset nel documento in C#.
type: docs
weight: 190
url: /it/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Esegue la stampa unione da un oggetto ADO Recordset nel documento.

```csharp
public void ExecuteADO(object recordset)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| recordset | Object | Oggetto Recordset ADO o record. |

## Osservazioni

Questo metodo è utile quando si intende utilizzare le classi Aspose.Words come oggetti COM da codice non gestito come un'applicazione creata utilizzando ASP o Visual Basic 6.0.

Questo metodo ignora il fileRemoveUnusedRegions opzione.

Per ulteriori informazioni vedere la descrizione di[`Execute`](../execute/).

## Esempi

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

Mostra come eseguire una stampa unione con i dati di un set di dati ADO.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

    // Per lavorare con ADO DataSets, dovremo aggiungere un riferimento alla libreria Microsoft ActiveX Data Objects,
    // che è incluso nella distribuzione .NET e archiviato in "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Crea una stringa di connessione che punta al file di database "Northwind".
    // nel nostro file system locale e apri una connessione.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Compila il nostro DataSet eseguendo un comando SQL sul nostro database.
    // I nomi delle colonne nella tabella dei risultati dovranno corrispondere
    // ai valori dei MERGEFIELDS che ospiteranno i nostri dati.
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Esegue la stampa unione e salva il documento.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Crea un documento vuoto e popolalo con MERGEFIELDS che accetterà i dati quando viene eseguita una stampa unione.
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

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
