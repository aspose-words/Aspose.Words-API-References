---
title: MailMerge.ExecuteWithRegions
second_title: Aspose.Words för .NET API Referens
description: MailMerge metod. Utför en koppling av epost från en anpassad datakälla med kopplingsregioner.
type: docs
weight: 200
url: /sv/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Utför en koppling av e-post från en anpassad datakälla med kopplingsregioner.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Ett objekt som implementerar det anpassade gränssnittet för kopplingsdatakällan. |

### Anmärkningar

Använd den här metoden för att fylla sammankopplingsfält i dokumentet med värden from alla anpassade datakällor som en XML-fil eller samlingar av affärsobjekt. Du måste skriva din egen klass som implementerar[`IMailMergeDataSource`](../../imailmergedatasource/) gränssnitt.

Du kan bara använda den här metoden när[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) är`falsk`, det vill säga att du inte behöver höger-till-vänster-språk (som arabiska eller hebreiska) kompatibilitet.

### Exempel

Visar hur man använder kopplingsregioner för att köra en kapslad koppling.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalt innehåller MERGEFIELDs namnet på en kolumn i en kopplingsdatakälla.
    // Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att starta/avsluta en kopplingsregion.
    // Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Dessa MERGEFIELDs finns i kopplingsområdet i tabellen "Kunder".
    // När vi kör sammankopplingen kommer detta fält att ta emot data från rader i en datakälla som heter "Kunder".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Skapa en andra kopplingsregion i den yttre regionen för en datakälla som heter "Beställningar".
    // Dataposterna "Beställningar" har en mång-till-en-relation med datakällan "Kunder".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Skapa relaterad data med namn som stämmer överens med våra kopplingsregioner.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // För att sammanfoga e-post från din datakälla måste vi slå in den i ett objekt som implementerar IMailMergeDataSource-gränssnittet.
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
/// Ett exempel på en maskinskriven samling som innehåller dina "data"-objekt.
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
/// Ett exempel på en underordnad "dataenhet"-klass i din applikation.
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
 /// En anpassad kopplingsdatakälla som du implementerar för att tillåta Aspose.Words
/// för att sammanfoga data från dina kundobjekt till Microsoft Word-dokument.
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
    /// Namnet på datakällan. Används endast av Aspose.Words när e-postsammanslagning med repeterbara regioner körs.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words anropar denna metod för att få ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words kopplingsmotor för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// En standardimplementation för att flytta till nästa post i en samling.
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
            // Hämta den underordnade datakällan, vars namn matchar kopplingsregionen som använder dess kolumner.
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
    /// Namnet på datakällan. Används endast av Aspose.Words när e-postsammanslagning med repeterbara regioner körs.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words anropar denna metod för att få ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words kopplingsmotor för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// En standardimplementation för att flytta till nästa post i en samling.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    /// <summary>
    /// Returnera null eftersom vi inte har några underordnade element för den här typen av objekt.
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
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Utför en koppling av e-post från en anpassad datakälla med kopplingsregioner.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Ett objekt som implementerar rotgränssnittet för den anpassade kopplingsdatakällan. |

### Anmärkningar

Använd den här metoden för att fylla sammankopplingsfält i dokumentet med värden from alla anpassade datakällor som en XML-fil eller samlingar av affärsobjekt. Du måste skriva dina egna classes som implementerar[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) och[`IMailMergeDataSource`](../../imailmergedatasource/) gränssnitt.

Du kan bara använda den här metoden när[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) är`falsk`, det vill säga att du inte behöver höger-till-vänster-språk (som arabiska eller hebreiska) kompatibilitet.

### Exempel

Utför sammanslagning från en anpassad datakälla med huvuddetaljdata.

```csharp
public void CustomDataSourceRoot()
{
    // Skapa ett dokument med två kopplingsregioner som heter "Washington" och "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Skapa två datakällor för kopplingen.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrera våra datakällor efter namn i en datakällas rot.
    // Om vi är på väg att använda denna datakällrot i en e-postsammanfogning med regioner,
    // Varje källas registrerade namn måste matcha namnet på en befintlig kopplingsregion i källdokumentet för kopplingen.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Eftersom vi har på varandra följande kopplingsregioner skulle vi normalt behöva utföra två kopplingar.
    // En kopplingskälla med en datarot kan dock fylla i flera regioner
    // om roten innehåller tabeller med motsvarande namn/kolumnnamn.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Skapa ett dokument som innehåller på varandra följande kopplingsregioner, med namn som anges av inmatningsmatrisen,
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
/// Ett exempel på en maskinskriven samling som innehåller dina "data"-objekt.
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
/// Datakällans rot som kan skickas direkt till en e-postkoppling som kan registrera och innehålla många underordnade datakällor.
/// Dessa källor måste alla implementera IMailMergeDataSource och är registrerade och differentierade med ett namn
/// som motsvarar en kopplingsregion som läser respektive data.
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
/// Anpassad kopplingsdatakälla.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// En standardimplementation för att flytta till nästa post i en samling.
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
    /// Namnet på datakällan. Används endast av Aspose.Words när e-postsammanslagning med repeterbara regioner körs.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words anropar denna metod för att få ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words kopplingsmotor för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Underordnade datakällor är för kapslade sammanslagningar.
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
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Utför sammanslagning från en **Dataset** till ett dokument med kopplingsregioner.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSet | DataSet | **Dataset** som innehåller data som ska infogas i kopplingsfält. |

### Anmärkningar

Använd den här metoden för att utföra sammankoppling av brev från en eller flera tabeller till repeterbara mail sammanfogningsområden i dokumentet. Kopplingsområdena i dokumentet kommer dynamiskt att växa för att rymma poster i motsvarande tabeller.

Varje bord i **Dataset** måste ha ett namn.

Dokumentet måste ha kopplingsregioner definierade med namn som hänvisar till tables i **Dataset**.

För att ange en kopplingsregion i dokumentet måste du infoga två kopplingsfält för att markera början och slutet av kopplingsområdet.

Allt dokumentinnehåll som ingår i en kopplingsregion kommer automatiskt att upprepas för varje post i **Datatabell**.

För att markera början av en kopplingsregion, infoga ett MERGEFIELD med namnet TableStart:MyTable, där MyTable motsvarar ett av tabellnamnen i din **Dataset**.

För att markera slutet av kopplingsområdet infogar du ett annat MERGEFIELD med namnet TableEnd:MyTable.

För att infoga ett MERGEFIELD i Word använd kommandot Insert/Field och välj MergeField och skriv sedan fältets namn.

De **TableStart** och **TableEnd** fält måste finnas i samma avsnitt i ditt dokument.

Om det används inuti ett bord, **TableStart** och **TableEnd** måste vara inne på samma rad i tabellen.

Kopplingsregioner i ett dokument bör vara väl utformade (det måste alltid finnas ett par matchning  **TableStart** och **TableEnd** slå samman fält med samma tabellnamn).

### Exempel

Visar hur man kör en kapslad e-postsammanfogning med två sammanfogningsregioner och två datatabeller.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalt innehåller MERGEFIELDs namnet på en kolumn i en kopplingsdatakälla.
    // Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att starta/avsluta en kopplingsregion.
    // Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Detta MERGEFIELD är inne i kopplingsområdet i tabellen "Kunder".
    // När vi kör sammankopplingen kommer detta fält att ta emot data från rader i en datakälla som heter "Kunder".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Skapa kolumnrubriker för en tabell som kommer att innehålla värden från en andra inre region.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Skapa en andra kopplingsregion i den yttre regionen för en tabell med namnet "Order".
    // Tabellen "Order" har en mång-till-en-relation med tabellen "Kunder" i kolumnen "Kund-ID".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Avsluta den inre regionen och avsluta sedan den yttre regionen. Öppnande och stängning av en kopplingsregion måste
    // händer på samma rad i en tabell.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Skapa en datauppsättning som innehåller de två tabellerna med de nödvändiga namnen och relationerna.
    // Varje sammanslagningsdokument för varje rad i tabellen "Kunder" i den yttre sammanslagningsregionen kommer att utföra sin sammanslagning i tabellen "Beställningar".
    // Varje sammanslagningsdokument visar alla rader i den senare tabellen vars kolumnvärden "Kund-ID" matchar den aktuella tabellraden "Kunder".
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Genererar en datamängd som har två datatabeller med namnet "Kunder" och "Beställningar", med en en-till-många-relation i kolumnen "Kund-ID".
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
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Utför sammanslagning från en **Datatabell** in i dokumentet med kopplingsregioner.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataTable | DataTable | Datakälla för sammankopplingsåtgärden. Tabellen must har sinTableName egenskapsuppsättning. |

### Anmärkningar

Dokumentet måste ha en kopplingsregion definierad med namn som matchar TableName.

Om det finns andra kopplingsområden definierade i dokumentet lämnas de intakta. Detta gör det möjligt att utföra flera kopplingsoperationer.

### Exempel

Demonstrerar hur man formaterar celler under en sammanfogning.

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
/// Formaterar tabellrader när en brevkoppling sker för att växla mellan två färger på udda/jämna rader.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en e-postsammanfogning slår samman data till ett MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Detta gäller om vi är i den första kolumnen, vilket betyder att vi har flyttat till en ny rad.
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
        // Göra ingenting.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Funktion som behövs för Visual Basic-autoportering som returnerar pariteten för det godkända numret.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Skapar en kopplingsdatakälla.
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

Visar hur man använder regioner för att utföra två separata sammanslagningar i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi vill utföra två sammanslagningar i följd på ett dokument samtidigt som vi tar data från två tabeller
// relaterade till varandra på något sätt, vi kan separera e-postsammanslagningarna med regioner.
// Normalt innehåller MERGEFIELDs namnet på en kolumn i en kopplingsdatakälla.
// Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att starta/avsluta en kopplingsregion.
// Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
// Dessa regioner är separata för orelaterade data, medan de kan kapslas för hierarkiska data.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Båda MERGEFIELD hänvisar till samma kolumnnamn, men värdena för var och en kommer från olika datatabeller.
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

// Vi kommer att behöva köra en sammanslagning per tabell. Den första sammanslagningen kommer att fylla MERGEFIELDs
// i "Städer"-intervallet medan fälten "Fruit"-intervallet inte är ifyllt.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Kör en andra sammanslagning för tabellen "Fruit", medan du använder en datavy
// för att sortera raderna i stigande ordning i kolumnen "Namn" före sammanfogningen.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Utför sammanslagning från en **DataView** in i dokumentet med kopplingsregioner.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataView | DataView | Datakälla för sammankopplingsåtgärden. Källtabellen för **DataView** måste ha sin **Tabellnamn** egenskapsuppsättning. |

### Anmärkningar

Den här metoden är användbar om du hämtar data till en **Datatabell** men då måste tillämpa ett filter eller sortera innan sammanslagningen.

Dokumentet måste ha en kopplingsregion definierad med namn som matchar  **DataView.Table.TableName**.

Om det finns andra kopplingsområden definierade i dokumentet lämnas de intakta. Detta gör det möjligt att utföra flera kopplingsoperationer.

### Exempel

Visar hur man använder regioner för att utföra två separata sammanslagningar i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi vill utföra två sammanslagningar i följd på ett dokument samtidigt som vi tar data från två tabeller
// relaterade till varandra på något sätt, vi kan separera e-postsammanslagningarna med regioner.
// Normalt innehåller MERGEFIELDs namnet på en kolumn i en kopplingsdatakälla.
// Istället kan vi använda prefixen "TableStart:" och "TableEnd:" för att starta/avsluta en kopplingsregion.
// Varje region kommer att tillhöra en tabell med ett namn som matchar strängen omedelbart efter prefixets kolon.
// Dessa regioner är separata för orelaterade data, medan de kan kapslas för hierarkiska data.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Båda MERGEFIELD hänvisar till samma kolumnnamn, men värdena för var och en kommer från olika datatabeller.
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

// Vi kommer att behöva köra en sammanslagning per tabell. Den första sammanslagningen kommer att fylla MERGEFIELDs
// i "Städer"-intervallet medan fälten "Fruit"-intervallet inte är ifyllt.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Kör en andra sammanslagning för tabellen "Fruit", medan du använder en datavy
// för att sortera raderna i stigande ordning i kolumnen "Namn" före sammanfogningen.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Utför sammanslagning från **IDataReader** in i dokumentet med kopplingsregioner.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataReader | IDataReader | Källa till dataposterna för sammanslagning som t.ex **OleDbDataReader** eller **SqlDataReader**. |
| tableName | String | Namn på kopplingsregionen i dokumentet som ska fyllas i. |

### Anmärkningar

Du kan passera **SqlDataReader** eller **OleDbDataReader**objekt till denna -metoden som en parameter eftersom de båda implementerade **IDataReader** gränssnitt.

### Exempel

Visar hur man infogar bilder lagrade i ett databas BLOB-fält i en rapport.

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
        // Göra ingenting.
    }

    /// <summary>
    /// Detta kallas när en sammanslagning stöter på ett MERGEFIELD i dokumentet med en "Image:"-tagg i sitt namn.
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
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)


