---
title: GetChildDataSource
second_title: Aspose.Words für .NET-API-Referenz
description: Die Aspose.Words-Serienbrief-Engine ruft diese Methode auf wenn sie auf den Beginn eines verschachtelten Seriendruckbereichs trifft.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Die Aspose.Words-Serienbrief-Engine ruft diese Methode auf, wenn sie auf den Beginn eines verschachtelten Seriendruckbereichs trifft.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | String | Der Name der Seriendruckregion, wie im Vorlagendokument angegeben. Groß- und Kleinschreibung beachten. |

### Rückgabewert

Ein Datenquellenobjekt, das Zugriff auf die Datensätze der angegebenen Tabelle bereitstellt.

### Bemerkungen

Wenn die Seriendruck-Engines von Aspose.Words einen Seriendruckbereich mit Daten füllt und auf den Anfang eines verschachtelten -Seriendruckbereichs in Form von MERGEFIELD TableStart:TableName stößt, wird sie aufgerufen`GetChildDataSource` auf dem Datenquellenobjekt current . Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben, das Zugriff auf die child -Datensätze des aktuellen übergeordneten Datensatzes bereitstellt. Aspose.Words verwendet die zurückgegebene Datenquelle, um den verschachtelten Seriendruckbereich aufzufüllen.

Unten sind die Regeln, die die Umsetzung von`GetChildDataSource` muss folgen.

Wenn die Tabelle, die durch dieses Datenquellenobjekt dargestellt wird, eine zugehörige untergeordnete Tabelle (Detailtabelle) mit dem angegebenen Namen hat, muss Ihre Implementierung eine neue zurückgeben[`IMailMergeDataSource`](../../imailmergedatasource) Objekt, das Zugriff auf die untergeordneten Datensätze des aktuellen Datensatzes bereitstellt. Ein Beispiel hierfür ist die Beziehung Orders / OrderDetails. Nehmen wir an, dass der Strom[`IMailMergeDataSource`](../../imailmergedatasource) object stellt die Orders-Tabelle dar und enthält einen aktuellen Order-Datensatz. Als nächstes trifft Aspose.Words auf „MERGEFIELD TableStart:OrderDetails“ im Dokument und ruft auf`GetChildDataSource` . Sie müssen eine erstellen und zurückgeben[`IMailMergeDataSource`](../../imailmergedatasource) -Objekt, das Aspose.Words den Zugriff auf den OrderDetails-Datensatz für die aktuelle Bestellung ermöglicht.

Wenn dieses Datenquellenobjekt keine Beziehung zu der Tabelle mit dem angegebenen Namen hat, müssen Sie a zurückgeben[`IMailMergeDataSource`](../../imailmergedatasource)Objekt, das Zugriff auf alle Datensätze der angegebenen Tabelle bereitstellt.

Wenn eine Tabelle mit dem angegebenen Namen nicht vorhanden ist, sollte Ihre Implementierung zurückkehren`Null` .

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

* interface [IMailMergeDataSource](../../imailmergedatasource)
* namensraum [Aspose.Words.MailMerging](../../imailmergedatasource)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
