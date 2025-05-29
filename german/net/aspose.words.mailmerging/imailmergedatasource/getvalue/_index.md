---
title: IMailMergeDataSource.GetValue
linktitle: GetValue
articleTitle: GetValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetValue-Methode von IMailMergeDataSource, um mühelos Feldwerte abzurufen oder „false“ zu erhalten, wenn sie nicht gefunden werden. Optimieren Sie noch heute Ihr Datenmanagement!
type: docs
weight: 30
url: /de/net/aspose.words.mailmerging/imailmergedatasource/getvalue/
---
## IMailMergeDataSource.GetValue method

Gibt einen Wert für den angegebenen Feldnamen zurück oder`FALSCH` wenn das Feld nicht gefunden wird.

```csharp
public bool GetValue(string fieldName, out object fieldValue)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Datenfeldes. |
| fieldValue | Object& | Gibt den Feldwert zurück. |

### Rückgabewert

`WAHR` wenn ein Wert gefunden wurde.

## Beispiele

Zeigt, wie ein Serienbrief mit einer Datenquelle in Form eines benutzerdefinierten Objekts ausgeführt wird.

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

        // Um ein benutzerdefiniertes Objekt als Datenquelle zu verwenden, muss es die Schnittstelle IMailMergeDataSource implementieren.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Ein Beispiel für eine „Datenentität“-Klasse in Ihrer Anwendung.
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
    /// Eine benutzerdefinierte Serienbrief-Datenquelle, die Sie implementieren, um Aspose.Words zu ermöglichen
/// um Daten aus Ihren Kundenobjekten per Serienbrief in Microsoft Word-Dokumente zu übertragen.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Wenn wir die Datenquelle initialisieren, muss ihre Position vor dem ersten Datensatz liegen.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Der Name der Datenquelle. Wird von Aspose.Words nur beim Ausführen von Serienbriefen mit wiederholbaren Bereichen verwendet.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um für jedes Datenfeld einen Wert zu erhalten.
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
                // Gibt "false" an die Aspose.Words-Serienbrief-Engine zurück, um anzuzeigen,
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Eine Standardimplementierung zum Wechseln zum nächsten Datensatz in einer Sammlung.
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

### Siehe auch

* interface [IMailMergeDataSource](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
