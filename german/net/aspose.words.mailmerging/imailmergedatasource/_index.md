---
title: IMailMergeDataSource Interface
linktitle: IMailMergeDataSource
articleTitle: IMailMergeDataSource
second_title: Aspose.Words für .NET
description: Aspose.Words.MailMerging.IMailMergeDataSource koppel. Implementieren Sie diese Schnittstelle um Serienbriefe aus einer benutzerdefinierten Datenquelle beispielsweise einer Liste von Objekten zu ermöglichen. MasterDetailDaten werden ebenfalls unterstützt in C#.
type: docs
weight: 3810
url: /de/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Implementieren Sie diese Schnittstelle, um Serienbriefe aus einer benutzerdefinierten Datenquelle, beispielsweise einer Liste von Objekten, zu ermöglichen. Master-Detail-Daten werden ebenfalls unterstützt.

```csharp
public interface IMailMergeDataSource
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | Gibt den Namen der Datenquelle zurück. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(*string*) | Die Mail-Merge-Engine von Aspose.Words ruft diese Methode auf, wenn sie auf den Anfang eines verschachtelten Mail-Merge-Bereichs stößt. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(*string, out object*) | Gibt einen Wert für den angegebenen Feldnamen oder zurück`FALSCH` wenn das Feld nicht gefunden wird. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Geht zum nächsten Datensatz in der Datenquelle. |

## Bemerkungen

Wenn eine Datenquelle erstellt wird, sollte sie so initialisiert werden, dass sie auf BOF verweist (vor dem ersten Datensatz). Die Mail-Merge-Engine Aspose.Words wird aufgerufen[`MoveNext`](./movenext/) um zum nächsten Datensatz zu gelangen und dann aufrufen[`GetValue`](./getvalue/) für jedes Serienbrieffeld, auf das es im Dokument oder im aktuellen Serienbriefbereich stößt.

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

     // Um ein benutzerdefiniertes Objekt als Datenquelle zu verwenden, muss es die IMailMergeDataSource-Schnittstelle implementieren.
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
/// um Seriendaten aus Ihren Kundenobjekten in Microsoft Word-Dokumente zu übertragen.
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
    /// Der Name der Datenquelle. Wird von Aspose.Words nur verwendet, wenn Serienbriefe mit wiederholbaren Bereichen ausgeführt werden.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld abzurufen.
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
                // „false“ an die Mail-Merge-Engine von Aspose.Words zurückgeben, um es zu kennzeichnen
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Eine Standardimplementierung zum Wechseln zu einem nächsten Datensatz in einer Sammlung.
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

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
