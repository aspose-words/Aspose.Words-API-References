---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die GetChildDataSource-Methode von IMailMergeDataSource den Serienbrief von Aspose.Words durch die nahtlose Verwaltung verschachtelter Bereiche verbessert.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Die Serienbrief-Engine von Aspose.Words ruft diese Methode auf, wenn sie auf den Anfang eines verschachtelten Serienbriefbereichs stößt.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | String | Der Name des Serienbriefbereichs, wie im Vorlagendokument angegeben. Groß-/Kleinschreibung wird nicht berücksichtigt. |

### Rückgabewert

Ein Datenquellenobjekt, das Zugriff auf die Datensätze der angegebenen Tabelle bietet.

## Bemerkungen

Wenn die Aspose.Words-Serienbrief-Engine einen Serienbriefbereich mit Daten füllt und auf den Anfang eines verschachtelten Serienbriefbereichs in der Form MERGEFIELD TableStart:TableName stößt, ruft sie`GetChildDataSource` auf dem aktuellen -Datenquellenobjekt. Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben, das Zugriff auf die untergeordneten -Datensätze des aktuellen übergeordneten Datensatzes ermöglicht. Aspose.Words verwendet die zurückgegebene Datenquelle, um den verschachtelten Seriendruckbereich zu füllen.

Nachfolgend sind die Regeln aufgeführt, die für die Umsetzung von`GetChildDataSource` muss folgen.

Wenn die Tabelle, die durch dieses Datenquellenobjekt dargestellt wird, eine zugehörige untergeordnete (Detail-)Tabelle mit dem angegebenen Namen hat, , dann muss Ihre Implementierung eine neue[`IMailMergeDataSource`](../) Objekt, das Zugriff auf die untergeordneten Datensätze des aktuellen Datensatzes gewährt. Ein Beispiel hierfür ist die Beziehung Orders / OrderDetails. Nehmen wir an, dass der aktuelle[`IMailMergeDataSource`](../) object repräsentiert die Tabelle „Bestellungen“ und enthält einen aktuellen Bestelldatensatz. Anschließend findet Aspose.Words „MERGEFIELD TableStart:OrderDetails“ im Dokument und ruft`GetChildDataSource` . Sie müssen eine[`IMailMergeDataSource`](../) -Objekt, das Aspose.Words den Zugriff auf den OrderDetails-Datensatz für die aktuelle Bestellung ermöglicht.

Wenn dieses Datenquellenobjekt keine Beziehung zur Tabelle mit dem angegebenen Namen hat, müssen Sie a[`IMailMergeDataSource`](../)Objekt, das Zugriff auf alle Datensätze der angegebenen Tabelle bietet.

Wenn eine Tabelle mit dem angegebenen Namen nicht existiert, sollte Ihre Implementierung zurückgeben`null` .

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
