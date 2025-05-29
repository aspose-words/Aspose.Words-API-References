---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words för .NET
description: Effektivisera ditt dokumentskapande med metoden MailMerge ExecuteWithRegions, vilket möjliggör effektiva dokumentkopplingar från anpassade datakällor och regioner.
type: docs
weight: 200
url: /sv/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

Utför en dokumentkoppling från en anpassad datakälla med områden för dokumentkoppling.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ett objekt som implementerar det anpassade gränssnittet för datakällan för dokumentkoppling. |

## Anmärkningar

Använd den här metoden för att fylla fält för koppling av dokument i dokumentet med värden från valfri anpassad datakälla, till exempel en XML-fil eller samlingar av affärsobjekt. Du måste skriva din egen klass som implementerar[`IMailMergeDataSource`](../../imailmergedatasource/) gränssnitt.

Du kan bara använda den här metoden när[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) är`falsk`, det vill säga, du behöver inte kompatibilitet med höger-till-vänster-språk (som arabiska eller hebreiska).

## Exempel

Visar hur man använder områden för dokumentkoppling för att köra en kapslad dokumentkoppling.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalt sett innehåller MERGEFIELD-fält namnet på en kolumn i en datakälla för dokumentkoppling.
    // Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att börja/avsluta en region för dokumentkoppling.
    // Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Dessa MERGEFIELD-fält finns inuti kopplingsområdet för dokument i tabellen "Kunder".
    // När vi kör dokumentkopplingen kommer det här fältet att ta emot data från rader i en datakälla med namnet "Kunder".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Skapa en andra region för dokumentkoppling inuti den yttre regionen för en datakälla med namnet "Ordrar".
    // Dataposterna "Ordrar" har en många-till-ett-relation med datakällan "Kunder".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Skapa relaterad data med namn som matchar namnen i våra regioner för dokumentkoppling.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // För att koppla dokument från din datakälla måste vi lägga in den i ett objekt som implementerar IMailMergeDataSource-gränssnittet.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Ett exempel på en "data entity"-klass i din applikation.
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
/// Ett exempel på en typad samling som innehåller dina "data"-objekt.
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
/// Ett exempel på en underklass "data entity" i din applikation.
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
 /// En anpassad datakälla för dokumentkoppling som du implementerar för att tillåta Aspose.Words
/// för att koppla data från dina kundobjekt till Microsoft Word-dokument.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // När vi initierar datakällan måste dess position vara före den första posten.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Namnet på datakällan. Används endast av Aspose.Words vid dokumentkoppling med repeterbara regioner.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words anropar den här metoden för att hämta ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words-kopplingsmotorn för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// En standardimplementering för att gå till nästa post i en samling.
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
            // Hämta den underordnade datakällan, vars namn matchar den region för dokumentkoppling som använder dess kolumner.
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

        // När vi initierar datakällan måste dess position vara före den första posten.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Namnet på datakällan. Används endast av Aspose.Words vid dokumentkoppling med repeterbara regioner.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words anropar den här metoden för att hämta ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words-kopplingsmotorn för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// En standardimplementering för att gå till nästa post i en samling.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    /// <summary>
    /// Returnera null eftersom vi inte har några underelement för den här typen av objekt.
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

### Se även

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

Utför en dokumentkoppling från en anpassad datakälla med områden för dokumentkoppling.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Ett objekt som implementerar det anpassade rotgränssnittet för datakällan för dokumentkoppling. |

## Anmärkningar

Använd den här metoden för att fylla fält för koppling av dokument i dokumentet med värden från vilken anpassad datakälla som helst, till exempel en XML-fil eller samlingar av affärsobjekt. Du måste skriva dina egna klasser som implementerar[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) och[`IMailMergeDataSource`](../../imailmergedatasource/) gränssnitt.

Du kan bara använda den här metoden när[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) är`falsk`, det vill säga, du behöver inte kompatibilitet med höger-till-vänster-språk (som arabiska eller hebreiska).

## Exempel

Utför dokumentkoppling från en anpassad datakälla med huvud-/detaljdata.

```csharp
public void CustomDataSourceRoot()
{
    // Skapa ett dokument med två kopplingsområden med namnet "Washington" och "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Skapa två datakällor för dokumentkopplingen.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrera våra datakällor med namn i en datakällrot.
    // Om vi ska använda den här datakällans rot i en dokumentkoppling med regioner,
    // varje källas registrerade namn måste matcha namnet på en befintlig region för dokumentkoppling i källdokumentet för dokumentkopplingen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Eftersom vi har områden för dokumentkopplingar som följer efter varandra, skulle vi normalt behöva utföra två dokumentkopplingar.
    // En enda källa för koppling av dokument med en datarot kan dock fylla i flera regioner
    // om roten innehåller tabeller med motsvarande namn/kolumnnamn.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Skapa ett dokument som innehåller efterföljande dokumentkopplingsområden, med namn som anges av inmatningsmatrisen,
/// för en datatabell över anställda.
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
/// Ett exempel på en "data entity"-klass i din applikation.
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
/// Ett exempel på en typad samling som innehåller dina "data"-objekt.
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
/// Datakällans rot som kan skickas direkt till en dokumentkoppling som kan registrera och innehålla många underordnade datakällor.
/// Dessa källor måste alla implementera IMailMergeDataSource och vara registrerade och differentierade med ett namn
/// vilket motsvarar ett område för dokumentkoppling som läser respektive data.
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
/// Anpassad datakälla för dokumentkoppling.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// En standardimplementering för att gå till nästa post i en samling.
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
    /// Namnet på datakällan. Används endast av Aspose.Words vid dokumentkoppling med repeterbara regioner.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words anropar den här metoden för att hämta ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words-kopplingsmotorn för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Underordnade datakällor är för kapslade dokumentkopplingar.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Se även

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

Utför koppling av dokument från en**Dataset** till ett dokument med områden för koppling av dokument.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSet | DataSet | **Dataset** som innehåller data som ska infogas i fält för koppling av dokument. |

## Anmärkningar

Använd den här metoden för att koppla dokument från en eller flera tabeller till repeterbara mail -kopplingsområden i dokumentet. De kopplade dokumentområdena i dokumentet kommer att växa dynamiskt för att rymma poster i motsvarande tabeller.

Varje bord i**Dataset** måste ha ett namn.

Dokumentet måste ha områden för koppling av dokument definierade med namn som refererar till tabellerna i**Dataset**.

För att ange ett område för koppling av dokument i dokumentet måste du infoga två fält för koppling av dokument för att markera början och slutet av området för koppling av dokument.

Allt dokumentinnehåll som ingår i ett dokumentkopplingsområde kommer automatiskt att upprepas för varje post i**Datatabell**.

För att markera början av ett kopplingsområde för dokument, infoga ett MERGEFIELD med namnet TableStart:MyTable, där MyTable motsvarar ett av tabellnamnen i din**Dataset**.

För att markera slutet på dokumentkopplingsområdet, infoga ett annat MERGEFIELD med namnet TableEnd:MyTable.

För att infoga ett MERGEFIELD i Word, använd kommandot Insert/Field och välj MergeField och skriv sedan namnet på fältet.

De**Tabellstart** och**Bordände** Fälten måste finnas inom samma avsnitt i dokumentet.

Om den används inuti en tabell,**Tabellstart** och**Bordände** måste finnas inom samma rad i tabellen.

Regioner för koppling av dokument i ett dokument bör vara välformade (det måste alltid finnas ett par matchande **Tabellstart** och**Bordände** sammanslagningsfält med samma tabellnamn).

## Exempel

Visar hur man utför en kapslad dokumentkoppling med två kopplingsområden och två datatabeller.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalt sett innehåller MERGEFIELD-fält namnet på en kolumn i en datakälla för dokumentkoppling.
    // Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att börja/avsluta en region för dokumentkoppling.
    // Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Detta MERGEFIELD finns inuti kopplingsområdet för dokument i tabellen "Kunder".
    // När vi kör dokumentkopplingen kommer det här fältet att ta emot data från rader i en datakälla med namnet "Kunder".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Skapa kolumnrubriker för en tabell som ska innehålla värden från en andra inre region.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Skapa en andra region för dokumentkoppling inuti den yttre regionen för en tabell med namnet "Ordrar".
    // Tabellen "Ordrar" har en många-till-ett-relation med tabellen "Kunder" i kolumnen "Kund-ID".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Avsluta den inre regionen och avsluta sedan den yttre regionen. Öppningen och stängningen av en kopplingsregion måste
    // hända på samma rad i en tabell.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Skapa en datauppsättning som innehåller de två tabellerna med de namn och relationer som krävs.
    // Varje kopplingsdokument för varje rad i tabellen "Kunder" i den yttre kopplingsregionen kommer att utföra sin dokumentkoppling på tabellen "Ordrar".
    // Varje sammanslagningsdokument visar alla rader i den senare tabellen vars kolumnvärden för "Kund-ID" matchar den aktuella raden i tabellen "Kunder".
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Genererar en datamängd som har två datatabeller med namnet "Kunder" och "Ordrar", med en en-till-många-relation i kolumnen "Kund-ID".
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

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

Utför koppling av dokument från en**Datatabell** i dokumentet med områden för koppling av dokument.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataTable | DataTable | Datakälla för dokumentkopplingsoperationen. Tabellen måste ha sinTableName egenskapsuppsättning. |

## Anmärkningar

Dokumentet måste ha ett område för dokumentkoppling definierat med ett namn som matchar TableName.

Om det finns andra områden för dokumentkoppling definierade i dokumentet lämnas de intakta. Detta gör det möjligt att utföra flera dokumentkopplingsåtgärder.

## Exempel

Visar hur man formaterar celler under en dokumentkoppling.

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
/// Formaterar tabellrader när en dokumentkoppling sker för att växla mellan två färger på udda/jämna rader.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en dokumentkoppling sammanfogar data till ett MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Detta gäller om vi är på den första kolumnen, vilket betyder att vi har flyttat till en ny rad.
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
        // Gör ingenting.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Funktion som behövs för Visual Basic-autoportering som returnerar pariteten för det skickade talet.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Skapar en datakälla för dokumentkoppling.
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

Visar hur man använder regioner för att köra två separata dokumentkopplingar i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi vill utföra två på varandra följande dokumentkopplingar på ett dokument samtidigt som vi hämtar data från två tabeller
// relaterade till varandra på något sätt kan vi separera dokumentkopplingarna med regioner.
// Normalt sett innehåller MERGEFIELD-fält namnet på en kolumn i en datakälla för dokumentkoppling.
// Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att börja/avsluta en region för dokumentkoppling.
// Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
// Dessa regioner är separata för orelaterad data, medan de kan kapslas för hierarkisk data.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Båda MERGEFIELD-värdena refererar till samma kolumnnamn, men värdena för varje kommer från olika datatabeller.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Skapa två orelaterade datatabeller.
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

// Vi behöver köra en dokumentkoppling per tabell. Den första dokumentkopplingen kommer att fylla i MERGEFIELDS
// i intervallet "Städer" medan fälten lämnas tomma i intervallet "Frukt".
doc.MailMerge.ExecuteWithRegions(tableCities);

// Kör en andra sammanslagning för tabellen "Frukt", medan du använder en datavyn
// för att sortera raderna i stigande ordning i kolumnen "Namn" före sammanslagningen.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

Utför koppling av dokument från en**Datavy** i dokumentet med områden för koppling av dokument.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataView | DataView | Datakälla för dokumentkopplingsoperationen. Källtabellen för**Datavy** måste ha sin**Tabellnamn** egenskapsuppsättning. |

## Anmärkningar

Den här metoden är användbar om du hämtar data till en**Datatabell** men sedan behöver du tillämpa ett filter eller en sortering innan dokumentkopplingen.

Dokumentet måste ha ett område för dokumentkoppling definierat med ett namn som matchar **DataView.Tabell.Tabellnamn**.

Om det finns andra områden för dokumentkoppling definierade i dokumentet lämnas de intakta. Detta gör det möjligt att utföra flera dokumentkopplingsåtgärder.

## Exempel

Visar hur man använder regioner för att köra två separata dokumentkopplingar i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi vill utföra två på varandra följande dokumentkopplingar på ett dokument samtidigt som vi hämtar data från två tabeller
// relaterade till varandra på något sätt kan vi separera dokumentkopplingarna med regioner.
// Normalt sett innehåller MERGEFIELD-fält namnet på en kolumn i en datakälla för dokumentkoppling.
// Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att börja/avsluta en region för dokumentkoppling.
// Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
// Dessa regioner är separata för orelaterad data, medan de kan kapslas för hierarkisk data.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Båda MERGEFIELD-värdena refererar till samma kolumnnamn, men värdena för varje kommer från olika datatabeller.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Skapa två orelaterade datatabeller.
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

// Vi behöver köra en dokumentkoppling per tabell. Den första dokumentkopplingen kommer att fylla i MERGEFIELDS
// i intervallet "Städer" medan fälten lämnas tomma i intervallet "Frukt".
doc.MailMerge.ExecuteWithRegions(tableCities);

// Kör en andra sammanslagning för tabellen "Frukt", medan du använder en datavyn
// för att sortera raderna i stigande ordning i kolumnen "Namn" före sammanslagningen.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

Utför koppling av dokument från**IDataläsare** i dokumentet med områden för koppling av dokument.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataReader | IDataReader | Källa för dataposterna för dokumentkoppling, till exempel**OleDbDataReader** eller**SqlDataReader**. |
| tableName | String | Namn på den kopplingsregion i dokumentet som ska fyllas i. |

## Anmärkningar

Du kan passera**SqlDataReader** eller**OleDbDataReader** objekt i this -metoden som parameter eftersom båda implementerade**IDataläsare** gränssnitt.

## Exempel

Visar hur man infogar bilder som lagras i ett BLOB-fält i en rapport.

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

        // Öppna dataläsaren, som måste vara i ett läge som läser alla poster samtidigt.
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
        // Gör ingenting.
    }

    /// <summary>
    /// Detta anropas när en dokumentkoppling stöter på ett MERGEFIELD i dokumentet med en "Image:"-tagg i namnet.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
