---
title: IMailMergeDataSource.TableName
second_title: Aspose.Words für .NET-API-Referenz
description: IMailMergeDataSource eigendom. Gibt den Namen der Datenquelle zurück.
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/imailmergedatasource/tablename/
---
## IMailMergeDataSource.TableName property

Gibt den Namen der Datenquelle zurück.

```csharp
public string TableName { get; }
```

### Rückgabewert

Der Name der Datenquelle. Leerer String, wenn die Datenquelle keinen Namen hat.

### Bemerkungen

Wenn Sie implementieren[`IMailMergeDataSource`](../), geben Sie den Namen der Quelle data aus dieser Eigenschaft zurück.

Aspose.Words verwendet diesen Namen, um ihn mit dem Namen der Seriendruckregion „specific “ im Vorlagendokument abzugleichen. Beim Vergleich zwischen dem Namen der Datenquelle und dem Namen der Seriendruckregion wird die Groß-/Kleinschreibung nicht beachtet.

### Beispiele

Zeigt, wie Sie einen Seriendruck mit einer Datenquelle in Form eines benutzerdefinierten Objekts ausführen.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    // Um ein benutzerdefiniertes Objekt als Datenquelle zu verwenden, muss es die IMailMergeDataSource-Schnittstelle implementieren. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Ein Beispiel für eine "Datenentitäts"-Klasse in Ihrer Anwendung.
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
/// Eine benutzerdefinierte Seriendatenquelle, die Sie implementieren, um Aspose.Words zuzulassen 
/// zum Seriendruck von Daten aus Ihren Kundenobjekten in Microsoft Word-Dokumente.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Wenn wir die Datenquelle initialisieren, muss ihre Position vor dem ersten Datensatz sein.
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
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld zu erhalten.
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
                // "false" an die Aspose.Words-Serienbrief-Engine zurückgeben, um dies zu kennzeichnen
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
* namensraum [Aspose.Words.MailMerging](../../imailmergedatasource/)
* Montage [Aspose.Words](../../../)


