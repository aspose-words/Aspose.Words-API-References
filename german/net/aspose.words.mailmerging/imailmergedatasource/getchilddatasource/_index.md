---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words für .NET
description: IMailMergeDataSource GetChildDataSource methode. Die MailMergeEngine von Aspose.Words ruft diese Methode auf wenn sie auf den Anfang eines verschachtelten MailMergeBereichs stößt in C#.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Die Mail-Merge-Engine von Aspose.Words ruft diese Methode auf, wenn sie auf den Anfang eines verschachtelten Mail-Merge-Bereichs stößt.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | String | Der Name des Serienbriefbereichs, wie im Vorlagendokument angegeben. Groß- und Kleinschreibung wird nicht beachtet. |

### Rückgabewert

Ein Datenquellenobjekt, das Zugriff auf die Datensätze der angegebenen Tabelle ermöglicht.

## Bemerkungen

Wenn die Mail-Merge-Engines von Aspose.Words einen Mail-Merge-Bereich mit Daten füllen und auf den Anfang eines verschachtelten Mail-Merge-Bereichs in der Form MERGEFIELD TableStart:TableName stoßen, wird dieser aufgerufen`GetChildDataSource` auf dem Datenquellenobjekt current . Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben, das Zugriff auf die child -Datensätze des aktuellen übergeordneten Datensatzes ermöglicht. Aspose.Words verwendet die zurückgegebene Datenquelle, um den verschachtelten Seriendruckbereich zu füllen.

Nachfolgend sind die Regeln aufgeführt, die für die Implementierung gelten`GetChildDataSource` muss folgen.

Wenn die Tabelle, die durch dieses Datenquellenobjekt dargestellt wird, eine zugehörige untergeordnete Tabelle (Detailtabelle) mit dem angegebenen Namen hat, muss Ihre Implementierung eine neue Tabelle zurückgeben[`IMailMergeDataSource`](../)Objekt, das Zugriff auf die untergeordneten Datensätze des aktuellen Datensatzes bereitstellt. Ein Beispiel hierfür ist die Orders/OrderDetails-Beziehung. Nehmen wir an, dass der Strom[`IMailMergeDataSource`](../) object stellt die Orders-Tabelle dar und verfügt über einen aktuellen Bestelldatensatz. Als nächstes trifft Aspose.Words auf „MERGEFIELD TableStart:OrderDetails“ im Dokument und ruft auf`GetChildDataSource` . Sie müssen eine erstellen und zurückgeben[`IMailMergeDataSource`](../) -Objekt, das Aspose.Words den Zugriff auf den OrderDetails-Datensatz für die aktuelle Bestellung ermöglicht.

Wenn dieses Datenquellenobjekt keine Beziehung zur Tabelle mit dem angegebenen Namen hat, müssen Sie a zurückgeben[`IMailMergeDataSource`](../) Objekt, das Zugriff auf alle Datensätze der angegebenen Tabelle bietet.

Wenn eine Tabelle mit dem angegebenen Namen nicht existiert, sollte Ihre Implementierung zurückkehren`Null` .

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

* interface [IMailMergeDataSource](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
