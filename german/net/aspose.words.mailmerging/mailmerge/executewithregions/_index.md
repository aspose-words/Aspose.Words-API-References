---
title: MailMerge.ExecuteWithRegions
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge methode. Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen durch.
type: docs
weight: 200
url: /de/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen durch.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ein Objekt, das die benutzerdefinierte Serienbrief-Datenquellenschnittstelle implementiert. |

### Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus jeder benutzerdefinierten Datenquelle wie einer XML-Datei oder Sammlungen von Geschäftsobjekten zu füllen. Sie müssen Ihre eigene Klasse schreiben, die das implementiert[`IMailMergeDataSource`](../../imailmergedatasource/) Schnittstelle.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) Ist`FALSCH`, Das heißt, Sie benötigen keine Rechts-nach-Links-Sprachkompatibilität (z. B. Arabisch oder Hebräisch).

### Beispiele

Zeigt, wie Sie Seriendruckbereiche verwenden, um einen verschachtelten Serienbrief auszuführen.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Serienbrief-Datenquelle.
    // Stattdessen können wir die Präfixe „TableStart:“ und „TableEnd:“ verwenden, um einen Seriendruckbereich zu beginnen/beenden.
    // Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfixes übereinstimmt.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Diese MERGEFIELDs befinden sich im Seriendruckbereich der Tabelle „Kunden“.
    // Wenn wir den Serienbrief ausführen, empfängt dieses Feld Daten aus Zeilen in einer Datenquelle namens „Kunden“.
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Erstellen Sie einen zweiten Serienbriefbereich innerhalb des äußeren Bereichs für eine Datenquelle namens „Orders“.
    // Die Dateneinträge „Bestellungen“ haben eine Viele-zu-Eins-Beziehung mit der Datenquelle „Kunden“.
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Erstellen Sie zugehörige Daten mit Namen, die denen unserer Serienbriefregionen entsprechen.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Um einen Serienbrief aus Ihrer Datenquelle zu versenden, müssen wir ihn in ein Objekt einbinden, das die IMailMergeDataSource-Schnittstelle implementiert.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
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
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// Ein Beispiel für eine typisierte Sammlung, die Ihre „Daten“-Objekte enthält.
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
/// Ein Beispiel für eine untergeordnete „Datenentität“-Klasse in Ihrer Anwendung.
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
 /// Eine benutzerdefinierte Serienbrief-Datenquelle, die Sie implementieren, um Aspose.Words zu ermöglichen
/// um Seriendaten aus Ihren Kundenobjekten in Microsoft Word-Dokumente zu übertragen.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
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
        get { return "Customers"; }
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
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
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
        switch (tableName)
        {
            // Holen Sie sich die untergeordnete Datenquelle, deren Name mit dem Serienbriefbereich übereinstimmt, der seine Spalten verwendet.
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

        // Wenn wir die Datenquelle initialisieren, muss ihre Position vor dem ersten Datensatz liegen.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Der Name der Datenquelle. Wird von Aspose.Words nur verwendet, wenn Serienbriefe mit wiederholbaren Bereichen ausgeführt werden.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld abzurufen.
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

    /// <summary>
    /// Null zurückgeben, da wir keine untergeordneten Elemente für diese Art von Objekt haben.
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

Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen durch.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Ein Objekt, das die Stammschnittstelle der benutzerdefinierten Serienbriefdatenquelle implementiert. |

### Bemerkungen

Verwenden Sie diese Methode, um Serienbrieffelder im Dokument mit Werten aus jeder benutzerdefinierten Datenquelle wie einer XML-Datei oder Sammlungen von Geschäftsobjekten zu füllen. Sie müssen Ihre eigenen Klassen schreiben, die das implementieren[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) Und[`IMailMergeDataSource`](../../imailmergedatasource/) Schnittstellen.

Sie können diese Methode nur verwenden, wenn[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) Ist`FALSCH`, Das heißt, Sie benötigen keine Rechts-nach-Links-Sprachkompatibilität (z. B. Arabisch oder Hebräisch).

### Beispiele

Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten durch.

```csharp
public void CustomDataSourceRoot()
{
    // Erstellen Sie ein Dokument mit zwei Serienbriefregionen namens „Washington“ und „Seattle“.
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Zwei Datenquellen für den Serienbrief erstellen.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrieren Sie unsere Datenquellen namentlich in einem Datenquellenstamm.
    // Wenn wir diesen Datenquellenstamm in einem Serienbrief mit Regionen verwenden möchten,
    // Der registrierte Name jeder Quelle muss mit dem Namen einer vorhandenen Serienbriefregion im Serienbrief-Quelldokument übereinstimmen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Da wir aufeinanderfolgende Serienbriefbereiche haben, müssten wir normalerweise zwei Serienbriefe durchführen.
    // Allerdings kann eine Serienbriefquelle mit einem Datenstamm mehrere Regionen ausfüllen
    // wenn die Wurzel Tabellen mit entsprechenden Namen/Spaltennamen enthält.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Erstellen Sie ein Dokument, das aufeinanderfolgende Serienbriefbereiche enthält, deren Namen durch das Eingabearray festgelegt werden.
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
/// Ein Beispiel für eine „Datenentität“-Klasse in Ihrer Anwendung.
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
/// Ein Beispiel für eine typisierte Sammlung, die Ihre „Daten“-Objekte enthält.
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
/// Datenquellenstamm, der direkt an einen Serienbrief übergeben werden kann, der viele untergeordnete Datenquellen registrieren und enthalten kann.
/// Diese Quellen müssen alle IMailMergeDataSource implementieren und werden durch einen Namen registriert und unterschieden
/// was einem Serienbriefbereich entspricht, der die entsprechenden Daten liest.
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
/// Benutzerdefinierte Serienbrief-Datenquelle.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
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

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// Der Name der Datenquelle. Wird von Aspose.Words nur verwendet, wenn Serienbriefe mit wiederholbaren Bereichen ausgeführt werden.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words ruft diese Methode auf, um einen Wert für jedes Datenfeld abzurufen.
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
                // „false“ an die Mail-Merge-Engine von Aspose.Words zurückgeben, um es zu kennzeichnen
                // dass wir kein Feld mit diesem Namen finden konnten.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Untergeordnete Datenquellen sind für verschachtelte Serienbriefe vorgesehen.
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

Führt einen Serienbrief von einem aus **Datensatz** in ein Dokument mit Seriendruckbereichen.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSet | DataSet | **Datensatz** das Daten enthält, die in Serienbrieffelder eingefügt werden sollen. |

### Bemerkungen

Verwenden Sie diese Methode, um einen Serienbrief aus einer oder mehreren Tabellen in wiederholbaren Mail -Zusammenführungsbereichen im Dokument durchzuführen. Die Seriendruckbereiche innerhalb des Dokuments werden dynamisch vergrößert, um Datensätze in den entsprechenden Tabellen aufzunehmen.

Jeder Tisch im **Datensatz** muss einen Namen haben.

Für das Dokument müssen Seriendruckbereiche definiert sein, deren Namen auf die Tabellen im Dokument verweisen **Datensatz**.

Um einen Seriendruckbereich im Dokument anzugeben, müssen Sie zwei Seriendruckfelder einfügen, um den Anfang und das Ende des Seriendruckbereichs zu markieren.

Der gesamte Dokumentinhalt, der in einem Serienbriefbereich enthalten ist, wird automatisch für jeden Datensatz im wiederholt **Datentabelle**.

Um den Anfang eines Serienbriefbereichs zu markieren, fügen Sie ein MERGEFIELD mit dem Namen TableStart:MyTable, ein, wobei MyTable einem der Tabellennamen in Ihrem entspricht **Datensatz**.

Um das Ende des Serienbriefbereichs zu markieren, fügen Sie ein weiteres MERGEFIELD mit dem Namen TableEnd:MyTable ein.

Um ein MERGEFIELD in Word einzufügen, verwenden Sie den Befehl „Einfügen/Feld“, wählen Sie „MergeField“ und geben Sie dann den -Namen des Felds ein.

Der **TableStart** Und **TableEnd** Felder müssen sich im selben Abschnitt Ihres Dokuments befinden.

Bei Verwendung innerhalb eines Tisches **TableStart** Und **TableEnd** muss sich in derselben Zeile der Tabelle befinden.

Seriendruckbereiche in einem Dokument sollten wohlgeformt sein (es muss immer ein Paar passender vorhanden sein). **TableStart** Und **TableEnd** Zusammenführungsfelder mit demselben Tabellennamen).

### Beispiele

Zeigt, wie ein verschachtelter Serienbrief mit zwei Zusammenführungsbereichen und zwei Datentabellen ausgeführt wird.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Serienbrief-Datenquelle.
    // Stattdessen können wir die Präfixe „TableStart:“ und „TableEnd:“ verwenden, um einen Seriendruckbereich zu beginnen/beenden.
    // Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfixes übereinstimmt.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Dieses MERGEFIELD befindet sich im Seriendruckbereich der Tabelle „Kunden“.
    // Wenn wir den Serienbrief ausführen, empfängt dieses Feld Daten aus Zeilen in einer Datenquelle namens „Kunden“.
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

    // Erstellen Sie einen zweiten Serienbriefbereich innerhalb des äußeren Bereichs für eine Tabelle mit dem Namen „Orders“.
    // Die Tabelle „Orders“ hat eine Viele-zu-Eins-Beziehung mit der Tabelle „Customers“ in der Spalte „CustomerID“.
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Beende den inneren Bereich und dann den äußeren Bereich. Das Öffnen und Schließen eines Serienbriefbereichs muss erfolgen
    // in derselben Zeile einer Tabelle passieren.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Einen Datensatz erstellen, der die beiden Tabellen mit den erforderlichen Namen und Beziehungen enthält.
    // Jedes Serienbriefdokument für jede Zeile der Tabelle „Kunden“ des äußeren Seriendruckbereichs führt seinen Serienbrief für die Tabelle „Bestellungen“ durch.
    // In jedem Zusammenführungsdokument werden alle Zeilen der letzteren Tabelle angezeigt, deren Spaltenwerte „CustomerID“ mit der aktuellen Tabellenzeile „Customers“ übereinstimmen.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Erzeugt einen Datensatz mit zwei Datentabellen namens „Customers“ und „Orders“ mit einer Eins-zu-viele-Beziehung in der Spalte „CustomerID“.
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

Führt einen Serienbrief von einem aus **Datentabelle** in das Dokument mit Seriendruckbereichen.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataTable | DataTable | Datenquelle für den Seriendruckvorgang. Die Tabelle muss habenTableName Eigenschaftssatz. |

### Bemerkungen

Für das Dokument muss ein Serienbriefbereich mit einem Namen definiert sein, der mit übereinstimmt.TableName.

Wenn im Dokument andere Seriendruckbereiche definiert sind, bleiben diese intakt. Dies ermöglicht die Durchführung mehrerer Serienbriefvorgänge.

### Beispiele

Demonstriert, wie Zellen während eines Seriendrucks formatiert werden.

```csharp
public void AlternatingRows()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");
}

/// <summary>
/// Formatiert Tabellenzeilen, während ein Seriendruck stattfindet, um zwischen zwei Farben in ungeraden/geraden Zeilen zu wechseln.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in einem MERGEFIELD zusammenführt.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Dies gilt, wenn wir uns in der ersten Spalte befinden, was bedeutet, dass wir in eine neue Zeile verschoben wurden.
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
/// Funktion, die für die automatische Portierung in Visual Basic benötigt wird und die Parität der übergebenen Zahl zurückgibt.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Erstellt eine Serienbrief-Datenquelle.
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

Zeigt, wie Regionen verwendet werden, um zwei separate Serienbriefe in einem Dokument auszuführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir zwei aufeinanderfolgende Serienbriefe für ein Dokument durchführen und dabei Daten aus zwei Tabellen übernehmen möchten
// in irgendeiner Weise miteinander in Beziehung stehen, können wir die Serienbriefe nach Regionen trennen.
// Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Serienbrief-Datenquelle.
// Stattdessen können wir die Präfixe „TableStart:“ und „TableEnd:“ verwenden, um einen Seriendruckbereich zu beginnen/beenden.
// Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfixes übereinstimmt.
// Diese Regionen sind für nicht verwandte Daten getrennt, während sie für hierarchische Daten verschachtelt werden können.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Beide MERGEFIELDs verweisen auf denselben Spaltennamen, die Werte für beide stammen jedoch aus unterschiedlichen Datentabellen.
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

// Wir müssen einen Serienbrief pro Tabelle ausführen. Beim ersten Serienbrief werden die MERGEFIELDs ausgefüllt
// im Bereich „Städte“, während die Felder im Bereich „Obst“ unbefüllt bleiben.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Führen Sie eine zweite Zusammenführung für die Tabelle „Fruit“ durch und verwenden Sie dabei eine Datenansicht
// um die Zeilen vor der Zusammenführung in aufsteigender Reihenfolge in der Spalte „Name“ zu sortieren.
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

Führt einen Serienbrief von einem aus **Datenansicht** in das Dokument mit Seriendruckbereichen.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataView | DataView | Datenquelle für den Seriendruckvorgang. Die Quelltabelle der **Datenansicht** muss es haben **Tabellenname** Eigenschaftssatz. |

### Bemerkungen

Diese Methode ist nützlich, wenn Sie Daten in a abrufen **Datentabelle** aber dann muss vor dem Seriendruck ein Filter oder eine Sortierung angewendet werden.

Für das Dokument muss ein Serienbriefbereich mit einem Namen definiert sein, der mit übereinstimmt. **DataView.Table.TableName**.

Wenn im Dokument andere Seriendruckbereiche definiert sind, bleiben diese intakt. Dies ermöglicht die Durchführung mehrerer Serienbriefvorgänge.

### Beispiele

Zeigt, wie Regionen verwendet werden, um zwei separate Serienbriefe in einem Dokument auszuführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir zwei aufeinanderfolgende Serienbriefe für ein Dokument durchführen und dabei Daten aus zwei Tabellen übernehmen möchten
// in irgendeiner Weise miteinander in Beziehung stehen, können wir die Serienbriefe nach Regionen trennen.
// Normalerweise enthalten MERGEFIELDs den Namen einer Spalte einer Serienbrief-Datenquelle.
// Stattdessen können wir die Präfixe „TableStart:“ und „TableEnd:“ verwenden, um einen Seriendruckbereich zu beginnen/beenden.
// Jede Region gehört zu einer Tabelle mit einem Namen, der mit der Zeichenfolge unmittelbar nach dem Doppelpunkt des Präfixes übereinstimmt.
// Diese Regionen sind für nicht verwandte Daten getrennt, während sie für hierarchische Daten verschachtelt werden können.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Beide MERGEFIELDs verweisen auf denselben Spaltennamen, die Werte für beide stammen jedoch aus unterschiedlichen Datentabellen.
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

// Wir müssen einen Serienbrief pro Tabelle ausführen. Beim ersten Serienbrief werden die MERGEFIELDs ausgefüllt
// im Bereich „Städte“, während die Felder im Bereich „Obst“ unbefüllt bleiben.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Führen Sie eine zweite Zusammenführung für die Tabelle „Fruit“ durch und verwenden Sie dabei eine Datenansicht
// um die Zeilen vor der Zusammenführung in aufsteigender Reihenfolge in der Spalte „Name“ zu sortieren.
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

Führt einen Serienbrief durch **IDataReader** in das Dokument mit Seriendruckbereichen.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataReader | IDataReader | Quelle der Datensätze für den Serienbrief wie z.B **OleDbDataReader** oder **SqlDataReader**. |
| tableName | String | Name des Seriendruckbereichs im Dokument, der gefüllt werden soll. |

### Bemerkungen

Du kannst passieren **SqlDataReader** oder **OleDbDataReader**Objekt als Parameter in die Methode this ein, da beide implementiert sind **IDataReader** Schnittstelle.

### Beispiele

Zeigt, wie in einem Datenbank-BLOB-Feld gespeicherte Bilder in einen Bericht eingefügt werden.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
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
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Nichts tun.
    }

    /// <summary>
    /// Dies wird aufgerufen, wenn ein Serienbrief im Dokument auf ein MERGEFIELD mit einem „Image:“-Tag im Namen trifft.
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


