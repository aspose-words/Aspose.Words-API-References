---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words per .NET
description: Semplifica la creazione dei tuoi documenti con il metodo MailMerge ExecuteWithRegionsADO. Unisci senza sforzo i dati dei Recordset ADO per risultati personalizzati.
type: docs
weight: 210
url: /it/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Esegue la stampa unione da un oggetto ADO Recordset nel documento con aree di stampa unione.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| recordset | Object | ADO Recordset o oggetto Record. |
| tableName | String | Nome dell'area di stampa unione nel documento da popolare. |

## Osservazioni

Questo metodo è utile quando si intende utilizzare le classi Aspose.Words come oggetti COM da codice non gestito, ad esempio un'applicazione creata utilizzando ASP o Visual Basic 6.0.

Per maggiori informazioni vedere la descrizione di[`ExecuteWithRegions`](../executewithregions/).

## Esempi

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

Mostra come eseguire una stampa unione con più regioni, compilata con dati da un set di dati ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // Per lavorare con i DataSet ADO, dovremo aggiungere un riferimento alla libreria Microsoft ActiveX Data Objects,
    // che è incluso nella distribuzione .NET e memorizzato in "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Crea una stringa di connessione che punta al file di database "Northwind"
    // nel nostro file system locale e apriamo una connessione.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Popoliamo il nostro DataSet eseguendo un comando SQL sul nostro database.
    // I nomi delle colonne nella tabella dei risultati dovranno corrispondere
    // ai valori dei MERGEFIELDS che ospiteranno i nostri dati.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Esegue una stampa unione solo sulla prima regione, riempiendo i suoi MERGEFIELDS con i dati del set di record.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Chiude il set di record e lo riapre con i dati di un'altra query SQL.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Esegui una seconda stampa unione sulla seconda area e salva il documento.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// Crea un documento con due aree di stampa unione.
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

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
