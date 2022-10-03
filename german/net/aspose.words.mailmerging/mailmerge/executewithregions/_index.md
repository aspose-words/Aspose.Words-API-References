---
title: ExecuteWithRegions
second_title: Aspose.Words für .NET-API-Referenz
description: Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Seriendruckregionen durch.
type: docs
weight: 200
url: /de/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Seriendruckregionen durch.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ein Objekt, das die benutzerdefinierte Seriendruck-Datenquellenschnittstelle implementiert. |

### Bemerkungen

Verwenden Sie diese Methode, um Seriendruckfelder im Dokument mit Werten aus einer beliebigen benutzerdefinierten Datenquelle wie einer XML-Datei oder Sammlungen von Geschäftsobjekten zu füllen. Sie müssen Ihre eigene Klasse schreiben, die die implementiert[`IMailMergeDataSource`](../../imailmergedatasource/) Schnittstelle.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)ist false, , das heißt, Sie benötigen keine Rechts-nach-links-Sprachkompatibilität (wie Arabisch oder Hebräisch).

### Beispiele

Zeigt, wie Seriendruckbereiche verwendet werden, um einen verschachtelten Seriendruck auszuführen.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Seriendruck-Datenquelle.
    // Stattdessen können wir die Präfixe "TableStart:" und "TableEnd:" verwenden, um einen Seriendruckbereich zu beginnen/zu beenden.
    // Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfix übereinstimmt.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Diese MERGEFIELDs befinden sich im Seriendruckbereich der Tabelle „Kunden“.
    // Wenn wir den Seriendruck ausführen, erhält dieses Feld Daten aus Zeilen in einer Datenquelle mit dem Namen "Kunden".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Einen zweiten Seriendruckbereich innerhalb des äußeren Bereichs für eine Datenquelle mit dem Namen "Bestellungen" erstellen.
    // Die Dateneinträge „Bestellungen“ haben eine Viele-zu-Eins-Beziehung mit der Datenquelle „Kunden“.
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Erstellen Sie verwandte Daten mit Namen, die denen unserer Seriendruckregionen entsprechen.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Für den Seriendruck aus Ihrer Datenquelle müssen wir sie in ein Objekt einschließen, das die IMailMergeDataSource-Schnittstelle implementiert.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
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
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// Ein Beispiel für eine typisierte Sammlung, die Ihre "Daten"-Objekte enthält.
/// </summary>
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer) base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Ein Beispiel einer untergeordneten "Datenentitäts"-Klasse in Ihrer Anwendung.
/// </summary>
public class Order
{
    public Order(string oName, int oQuantity)
    {
        Name = oName;
        Quantity = oQuantity;
    }

    public string Name { get; set; }
    public int Quantity { get; set; }
}

/// <summary>
/// Eine benutzerdefinierte Seriendatenquelle, die Sie implementieren, um Aspose.Words zuzulassen 
/// zum Seriendruck von Daten aus Ihren Kundenobjekten in Microsoft Word-Dokumente.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
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
        get { return "Customers"; }
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
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
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
        switch (tableName)
        {
            // Abrufen der untergeordneten Datenquelle, deren Name mit der Seriendruckregion übereinstimmt, die ihre Spalten verwendet.
            case "Orders":
                return new OrderMailMergeDataSource(mCustomers[mRecordIndex].Orders);
            default:
                return null;
        }
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly CustomerList mCustomers;
    private int mRecordIndex;
}

public class OrderMailMergeDataSource : IMailMergeDataSource
{
    public OrderMailMergeDataSource(List<Order> orders)
    {
        mOrders = orders;

        // Wenn wir die Datenquelle initialisieren, muss ihre Position vor dem ersten Datensatz sein.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Der Name der Datenquelle. Wird von Aspose.Words nur beim Ausführen von Serienbriefen mit wiederholbaren Bereichen verwendet.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld zu erhalten.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "Name":
                fieldValue = mOrders[mRecordIndex].Name;
                return true;
            case "Quantity":
                fieldValue = mOrders[mRecordIndex].Quantity;
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

    /// <summary>
    /// Null zurückgeben, weil wir keine untergeordneten Elemente für diese Art von Objekt haben.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mOrders.Count); }
    }

    private readonly List<Order> mOrders;
    private int mRecordIndex;
}
```

### Siehe auch

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Seriendruckregionen durch.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Ein Objekt, das die Stammschnittstelle der benutzerdefinierten Seriendruck-Datenquelle implementiert. |

### Bemerkungen

Verwenden Sie diese Methode, um Seriendruckfelder im Dokument mit Werten aus einer beliebigen benutzerdefinierten Datenquelle wie einer XML-Datei oder Sammlungen von Geschäftsobjekten zu füllen. Sie müssen Ihre eigenen Klassen schreiben, die die implementieren[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) und[`IMailMergeDataSource`](../../imailmergedatasource/) Schnittstellen.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)ist false, , das heißt, Sie benötigen keine Rechts-nach-links-Sprachkompatibilität (wie Arabisch oder Hebräisch).

### Beispiele

Führt den Seriendruck aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten durch.

```csharp
public void CustomDataSourceRoot()
{
    // Erstellen Sie ein Dokument mit zwei Seriendruckregionen namens "Washington" und "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Erstellen Sie zwei Datenquellen für den Seriendruck.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Unsere Datenquellen namentlich in einem Datenquellenstamm registrieren.
    // Wenn wir im Begriff sind, diesen Datenquellenstamm in einem Seriendruck mit Regionen zu verwenden,
    // Der registrierte Name jeder Quelle muss mit dem Namen einer bestehenden Serienbriefregion im Serienbrief-Quelldokument übereinstimmen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Da wir aufeinanderfolgende Serienbriefregionen haben, müssten wir normalerweise zwei Serienbriefe durchführen.
    // Eine Seriendruckquelle mit einem Datenstamm kann jedoch mehrere Regionen ausfüllen
    // wenn die Wurzel Tabellen mit entsprechenden Namen/Spaltennamen enthält.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Erstellen Sie ein Dokument, das aufeinanderfolgende Seriendruckbereiche enthält, mit Namen, die durch das Eingabearray bestimmt werden,
/// für eine Datentabelle von Mitarbeitern.
/// </summary>
private static Document CreateSourceDocumentWithMailMergeRegions(string[] regions)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    foreach (string s in regions)
    {
        builder.Writeln("\n" + s + " branch: ");
        builder.InsertField(" MERGEFIELD TableStart:" + s);
        builder.InsertField(" MERGEFIELD FullName");
        builder.Write(", ");
        builder.InsertField(" MERGEFIELD Department");
        builder.InsertField(" MERGEFIELD TableEnd:" + s);
    }

    return doc;
}

/// <summary>
/// Ein Beispiel für eine "Datenentitäts"-Klasse in Ihrer Anwendung.
/// </summary>
private class Employee
{
    public Employee(string aFullName, string aDepartment)
    {
        FullName = aFullName;
        Department = aDepartment;
    }

    public string FullName { get; }
    public string Department { get; }
}

/// <summary>
/// Ein Beispiel für eine typisierte Sammlung, die Ihre "Daten"-Objekte enthält.
/// </summary>
private class EmployeeList : ArrayList
{
    public new Employee this[int index]
    {
        get { return (Employee)base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Datenquellenstamm, der direkt an einen Seriendruck übergeben werden kann, der viele untergeordnete Datenquellen registrieren und enthalten kann.
/// Diese Quellen müssen alle IMailMergeDataSource implementieren und werden durch einen Namen registriert und unterschieden
/// was einem Seriendruckbereich entspricht, der die jeweiligen Daten liest.
/// </summary>
private class DataSourceRoot : IMailMergeDataSourceRoot
{
    public IMailMergeDataSource GetDataSource(string tableName)
    {
        EmployeeListMailMergeSource source = mSources[tableName];
        source.Reset();
        return mSources[tableName];
    }

    public void RegisterSource(string sourceName, EmployeeListMailMergeSource source)
    {
        mSources.Add(sourceName, source);
    }

    private readonly Dictionary<string, EmployeeListMailMergeSource> mSources = new Dictionary<string, EmployeeListMailMergeSource>();
}

/// <summary>
/// Benutzerdefinierte Datenquelle für Serienbriefe.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
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

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// Der Name der Datenquelle. Wird von Aspose.Words nur beim Ausführen von Serienbriefen mit wiederholbaren Bereichen verwendet.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld zu erhalten.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mEmployees[mRecordIndex].FullName;
                return true;
            case "Department":
                fieldValue = mEmployees[mRecordIndex].Department;
                return true;
            default:
                // "false" an die Aspose.Words-Serienbrief-Engine zurückgeben, um dies zu kennzeichnen
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Untergeordnete Datenquellen sind für verschachtelte Serienbriefe.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Siehe auch

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Führt den Seriendruck aus einem DataSet in ein Dokument mit Seriendruckbereichen durch.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSet | DataSet | DataSet, das Daten enthält, die in Seriendruckfelder eingefügt werden sollen. |

### Bemerkungen

Verwenden Sie diese Methode, um einen Seriendruck aus einer oder mehreren Tabellen in wiederholbare Seriendruckbereiche im Dokument auszuführen. Die Seriendruckbereiche innerhalb des Dokuments werden dynamisch größer, um Datensätze in den entsprechenden Tabellen aufzunehmen.

Jede Tabelle im DataSet muss einen Namen haben.

Das Dokument muss über definierte Seriendruckbereiche mit Namen verfügen, die auf die tables im DataSet verweisen.

Um einen Seriendruckbereich im Dokument festzulegen, müssen Sie zwei Seriendruckfelder einfügen, um den Anfang und das Ende des Seriendruckbereichs zu markieren.

Alle Dokumentinhalte, die in einem Seriendruckbereich enthalten sind, werden automatisch für jeden Datensatz in der DataTable wiederholt.

Um den Anfang eines Seriendruckbereichs zu markieren, fügen Sie ein MERGEFIELD mit dem Namen TableStart:MyTable, ein, wobei MyTable einem der Tabellennamen in Ihrem DataSet entspricht.

Um das Ende des Seriendruckbereichs zu markieren, fügen Sie ein weiteres MERGEFIELD mit dem Namen TableEnd:MyTable ein.

Um ein MERGEFIELD in Word einzufügen, verwenden Sie den Befehl Insert/Field und wählen Sie MergeField und geben Sie dann den Namen des Felds ein.

Die Felder TableStart und TableEnd müssen sich in Ihrem Dokument im selben Abschnitt befinden.

Bei Verwendung innerhalb einer Tabelle müssen sich TableStart und TableEnd in derselben Zeile der Tabelle befinden.

Seriendruckbereiche in einem Dokument sollten wohlgeformt sein (es muss immer ein Paar zusammenpassender Tabellenstart- und Tabellenend-Briefvorlagenfelder mit demselben Tabellennamen vorhanden sein).

### Beispiele

Zeigt, wie ein verschachtelter Seriendruck mit zwei Zusammenführungsbereichen und zwei Datentabellen ausgeführt wird.

```csharp
[Test]
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Seriendruck-Datenquelle.
    // Stattdessen können wir die Präfixe "TableStart:" und "TableEnd:" verwenden, um einen Seriendruckbereich zu beginnen/zu beenden.
    // Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfix übereinstimmt.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Dieses MERGEFIELD befindet sich im Seriendruckbereich der Tabelle "Kunden".
    // Wenn wir den Seriendruck ausführen, erhält dieses Feld Daten aus Zeilen in einer Datenquelle mit dem Namen "Kunden".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Spaltenüberschriften für eine Tabelle erstellen, die Werte aus einem zweiten inneren Bereich enthält.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Erstellen Sie einen zweiten Seriendruckbereich innerhalb des äußeren Bereichs für eine Tabelle mit dem Namen "Bestellungen".
    // Die Tabelle „Bestellungen“ hat eine Viele-zu-Eins-Beziehung mit der Tabelle „Kunden“ in der Spalte „Kunden-ID“.
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Beende die innere Region und dann die äußere Region. Das Öffnen und Schließen eines Serienbriefbereichs muss
    // geschieht in derselben Zeile einer Tabelle.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Erstellen Sie ein Dataset, das die beiden Tabellen mit den erforderlichen Namen und Beziehungen enthält.
    // Jedes Zusammenführungsdokument für jede Zeile der Tabelle „Kunden“ des äußeren Zusammenführungsbereichs führt seinen Seriendruck für die Tabelle „Bestellungen“ durch.
    // Jedes Zusammenführungsdokument zeigt alle Zeilen der letztgenannten Tabelle an, deren "CustomerID"-Spaltenwerte mit der aktuellen "Customers"-Tabellenzeile übereinstimmen.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Generiert einen Datensatz mit zwei Datentabellen namens „Kunden“ und „Bestellungen“ mit einer 1:n-Beziehung in der Spalte „Kunden-ID“.
/// </summary>
private static DataSet CreateDataSet()
{
    DataTable tableCustomers = new DataTable("Customers");
    tableCustomers.Columns.Add("CustomerID");
    tableCustomers.Columns.Add("CustomerName");
    tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
    tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

    DataTable tableOrders = new DataTable("Orders");
    tableOrders.Columns.Add("CustomerID");
    tableOrders.Columns.Add("ItemName");
    tableOrders.Columns.Add("Quantity");
    tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
    tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
    tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

    DataSet dataSet = new DataSet();
    dataSet.Tables.Add(tableCustomers);
    dataSet.Tables.Add(tableOrders);
    dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

    return dataSet;
}
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Führt den Seriendruck aus einer DataTable in das Dokument mit Seriendruckbereichen durch.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataTable | DataTable | Datenquelle für den Seriendruckvorgang. Die Tabelle muss haben **Tabellenname** Eigenschaftssatz. |

### Bemerkungen

Für das Dokument muss ein Seriendruckbereich definiert sein, dessen Name mit übereinstimmt. **Datentabelle.Tabellenname**.

Wenn im Dokument andere Seriendruckbereiche definiert sind, bleiben sie intakt. Dadurch können mehrere Seriendruckvorgänge durchgeführt werden.

### Beispiele

Veranschaulicht, wie Zellen während eines Seriendrucks formatiert werden.

```csharp
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");

/// <summary>
/// Formatiert Tabellenzeilen, wenn ein Seriendruck stattfindet, um zwischen zwei Farben in ungeraden/geraden Zeilen zu wechseln.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn bei einem Seriendruck Daten in einem MERGEFIELD zusammengeführt werden.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Dies gilt, wenn wir uns in der ersten Spalte befinden, was bedeutet, dass wir uns in eine neue Zeile bewegt haben.
        if (args.FieldName == "CompanyName")
        {
            Color rowColor = IsOdd(mRowIdx) ? Color.FromArgb(213, 227, 235) : Color.FromArgb(242, 242, 242);

            for (int colIdx = 0; colIdx < 4; colIdx++)
            {
                mBuilder.MoveToCell(0, mRowIdx, colIdx, 0);
                mBuilder.CellFormat.Shading.BackgroundPatternColor = rowColor;
            }

            mRowIdx++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Nichts tun.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Für Visual Basic Autoporting benötigte Funktion, die die Parität der übergebenen Zahl zurückgibt.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Erstellt eine Seriendruck-Datenquelle.
/// </summary>
private static DataTable GetSuppliersDataTable()
{
    DataTable dataTable = new DataTable("Suppliers");
    dataTable.Columns.Add("CompanyName");
    dataTable.Columns.Add("ContactName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Company " + i;
        datarow[1] = "Contact " + i;
    }

    return dataTable;
}
```

Zeigt, wie Bereiche verwendet werden, um zwei separate Serienbriefe in einem Dokument auszuführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir zwei aufeinanderfolgende Seriendrucke für ein Dokument durchführen wollen, während Daten aus zwei Tabellen genommen werden
// in irgendeiner Weise miteinander in Verbindung stehen, können wir die Serienbriefe nach Regionen trennen.
// Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Seriendruck-Datenquelle.
// Stattdessen können wir die Präfixe "TableStart:" und "TableEnd:" verwenden, um einen Seriendruckbereich zu beginnen/zu beenden.
// Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfix übereinstimmt.
// Diese Regionen sind für nicht zusammenhängende Daten getrennt, während sie für hierarchische Daten verschachtelt werden können.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Beide MERGEFIELDs beziehen sich auf denselben Spaltennamen, aber die Werte für beide stammen aus unterschiedlichen Datentabellen.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Zwei unabhängige Datentabellen erstellen.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Wir müssen einen Seriendruck pro Tabelle ausführen. Der erste Seriendruck füllt die MERGEFIELDs
// im Bereich "Städte", während die Felder im Bereich "Obst" ungefüllt bleiben.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Führen Sie eine zweite Zusammenführung für die Tabelle "Obst" aus, während Sie eine Datenansicht verwenden
// zum Sortieren der Zeilen in aufsteigender Reihenfolge in der Spalte "Name" vor der Zusammenführung.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Führt den Seriendruck von einer DataView in das Dokument mit Seriendruckbereichen durch.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataView | DataView | Datenquelle für den Seriendruckvorgang. Die Quelltabelle der **Datenansicht** muss sein **Tabellenname** Eigenschaftssatz. |

### Bemerkungen

Diese Methode ist nützlich, wenn Sie Daten in a abrufen **Datentabelle** aber then muss vor dem Seriendruck einen Filter oder eine Sortierung anwenden.

Für das Dokument muss ein Seriendruckbereich definiert sein, dessen Name mit übereinstimmt. **DataView.Tabelle.Tabellenname**.

Wenn im Dokument andere Seriendruckbereiche definiert sind, bleiben sie intakt. Dadurch können mehrere Seriendruckvorgänge durchgeführt werden.

### Beispiele

Zeigt, wie Bereiche verwendet werden, um zwei separate Serienbriefe in einem Dokument auszuführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir zwei aufeinanderfolgende Seriendrucke für ein Dokument durchführen wollen, während Daten aus zwei Tabellen genommen werden
// in irgendeiner Weise miteinander in Verbindung stehen, können wir die Serienbriefe nach Regionen trennen.
// Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Seriendruck-Datenquelle.
// Stattdessen können wir die Präfixe "TableStart:" und "TableEnd:" verwenden, um einen Seriendruckbereich zu beginnen/zu beenden.
// Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfix übereinstimmt.
// Diese Regionen sind für nicht zusammenhängende Daten getrennt, während sie für hierarchische Daten verschachtelt werden können.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Beide MERGEFIELDs beziehen sich auf denselben Spaltennamen, aber die Werte für beide stammen aus unterschiedlichen Datentabellen.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Zwei unabhängige Datentabellen erstellen.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Wir müssen einen Seriendruck pro Tabelle ausführen. Der erste Seriendruck füllt die MERGEFIELDs
// im Bereich "Städte", während die Felder im Bereich "Obst" ungefüllt bleiben.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Führen Sie eine zweite Zusammenführung für die Tabelle "Obst" aus, während Sie eine Datenansicht verwenden
// zum Sortieren der Zeilen in aufsteigender Reihenfolge in der Spalte "Name" vor der Zusammenführung.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Führt den Seriendruck von IDataReader in das Dokument mit Seriendruckbereichen durch.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataReader | IDataReader | Quelle der Datensätze für den Seriendruck wie OleDbDataReader oder SqlDataReader. |
| tableName | String | Name des Seriendruckbereichs im zu füllenden Dokument. |

### Bemerkungen

Du kannst passieren **SqlDataReader** oder **OleDbDataReader** Objekt in die Methode this als Parameter, da sie beide implementiert sind **IDataReader** Schnittstelle.

### Beispiele

Zeigt, wie in einem Datenbank-BLOB-Feld gespeicherte Bilder in einen Bericht eingefügt werden.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Öffnen Sie den Datenleser, der sich in einem Modus befinden muss, der alle Datensätze auf einmal liest.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Nichts tun.
    }

    /// <summary>
    /// Dies wird aufgerufen, wenn ein Seriendruck auf ein MERGEFIELD im Dokument mit einem "Image:"-Tag im Namen trifft.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
