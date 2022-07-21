---
title: IMailMergeDataSource
second_title: Aspose.Words für .NET-API-Referenz
description: Implementieren Sie diese Schnittstelle um den Seriendruck aus einer benutzerdefinierten Datenquelle zuzulassen z. B. einer Liste von Objekten. Master-Detail-Daten werden ebenfalls unterstützt.
type: docs
weight: 3590
url: /de/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Implementieren Sie diese Schnittstelle, um den Seriendruck aus einer benutzerdefinierten Datenquelle zuzulassen, z. B. einer Liste von Objekten. Master-Detail-Daten werden ebenfalls unterstützt.

```csharp
public interface IMailMergeDataSource
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename) { get; } | Gibt den Namen der Datenquelle zurück. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource)(string) | Die Aspose.Words-Serienbrief-Engine ruft diese Methode auf, wenn sie auf den Beginn eines verschachtelten Seriendruckbereichs trifft. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue)(string, out object) | Gibt einen Wert für den angegebenen Feldnamen zurück oder false, wenn das Feld nicht gefunden wird. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext)() | Geht zum nächsten Datensatz in der Datenquelle vor. |

### Bemerkungen

Wenn eine Datenquelle erstellt wird, sollte sie so initialisiert werden, dass sie auf BOF (vor dem ersten Datensatz) zeigt. Die Aspose.Words-Serienbrief-Engine wird aufgerufen[`MoveNext`](./movenext) um zum nächsten Datensatz vorzurücken und dann aufzurufen[`GetValue`](./getvalue) für jedes Briefvorlagenfeld, auf das es im Dokument oder im aktuellen Seriendruckbereich trifft.

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

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
