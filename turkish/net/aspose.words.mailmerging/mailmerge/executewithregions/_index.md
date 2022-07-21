---
title: ExecuteWithRegions
second_title: Aspose.Words for .NET API Referansı
description: Adres mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres mektup birleştirme gerçekleştirir.
type: docs
weight: 200
url: /tr/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Adres mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Özel adres mektup birleştirme veri kaynağı arabirimini uygulayan bir nesne. |

### Notlar

Belgedeki adres mektup birleştirme alanlarını XML dosyası veya iş nesneleri koleksiyonları gibi herhangi bir özel veri kaynağından gelen değerleriyle doldurmak için bu yöntemi kullanın. Şunu uygulayan your kendi sınıfınızı yazmanız gerekir.[`IMailMergeDataSource`](../../imailmergedatasource) arayüz.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)false, yani Sağdan Sola dil (Arapça veya İbranice gibi) uyumluluğuna ihtiyacınız yoktur.

### Örnekler

İç içe adres mektup birleştirme yürütmek için adres mektup birleştirme bölgelerinin nasıl kullanılacağını gösterir.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalde, MERGEFIELD'ler adres mektup birleştirme veri kaynağının bir sütununun adını içerir.
    // Bunun yerine, adres mektup birleştirme bölgesini başlatmak/sonlandırmak için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
    // Her bölge, önek iki nokta üst üste işaretinden hemen sonraki dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Bu MERGEFIELD'ler, "Müşteriler" tablosunun adres mektup birleştirme bölgesinin içindedir.
    // Adres mektup birleştirmeyi gerçekleştirdiğimizde, bu alan "Müşteriler" adlı bir veri kaynağındaki satırlardan veri alacaktır.
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // "Siparişler" adlı bir veri kaynağı için dış bölge içinde ikinci bir adres mektup birleştirme bölgesi oluşturun.
    // "Siparişler" veri girişleri, "Müşteriler" veri kaynağı ile çoktan bire bir ilişkiye sahiptir.
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Adres mektup birleştirme bölgelerimizle eşleşen adlarla ilgili verileri oluşturun.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Veri kaynağınızdan adres mektup birleştirme için, onu IMailMergeDataSource arabirimini uygulayan bir nesneye sarmamız gerekir.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Uygulamanızda bir "veri varlığı" sınıfı örneği.
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
/// "veri" nesnelerinizi içeren bir yazılı koleksiyon örneği.
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
/// Uygulamanızdaki bir alt "veri varlığı" sınıfı örneği.
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
/// Aspose.Words'e izin vermek için uyguladığınız özel bir adres mektup birleştirme veri kaynağı 
/// Müşteri nesnelerinizden Microsoft Word belgelerine adres mektup birleştirme verileri.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // Veri kaynağını başlattığımızda, konumu ilk kayıttan önce olmalıdır.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle adres mektup birleştirme yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words, her veri alanı için bir değer almak için bu yöntemi çağırır.
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
                // Belirtmek için Aspose.Words adres mektup birleştirme motoruna "false" döndür
                // bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
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
            // Adı sütunlarını kullanan adres mektup birleştirme bölgesiyle eşleşen alt veri kaynağını alın.
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

        // Veri kaynağını başlattığımızda, konumu ilk kayıttan önce olmalıdır.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle adres mektup birleştirme yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words, her veri alanı için bir değer almak için bu yöntemi çağırır.
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
                // Belirtmek için Aspose.Words adres mektup birleştirme motoruna "false" döndür
                // bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    /// <summary>
    /// Bu tür nesneler için herhangi bir alt öğemiz olmadığı için null döndürün.
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

### Ayrıca bakınız

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Adres mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Özel adres mektup birleştirme veri kaynağı kök arabirimini uygulayan bir nesne. |

### Notlar

Belgedeki adres mektup birleştirme alanlarını XML dosyası veya iş nesneleri koleksiyonları gibi herhangi bir özel veri kaynağından gelen değerleriyle doldurmak için bu yöntemi kullanın. Bunu uygulayan kendi sınıflarınızı yazmanız gerekir.[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot) ve[`IMailMergeDataSource`](../../imailmergedatasource) arayüzler.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)false, yani Sağdan Sola dil (Arapça veya İbranice gibi) uyumluluğuna ihtiyacınız yoktur.

### Örnekler

Ana ayrıntı verileriyle özel bir veri kaynağından adres mektup birleştirme gerçekleştirir.

```csharp
public void CustomDataSourceRoot()
{
    // "Washington" ve "Seattle" adlı iki adres mektup birleştirme bölgesine sahip bir belge oluşturun.
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Adres mektup birleştirme için iki veri kaynağı oluşturun.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Veri kaynaklarımızı bir veri kaynağı köküne ada göre kaydedin.
    // Bu veri kaynağı kökünü bölgelerle adres mektup birleştirmede kullanmak üzereysek,
    // her kaynağın kayıtlı adı, adres mektup birleştirme kaynak belgesindeki mevcut bir adres mektup birleştirme bölgesinin adıyla eşleşmelidir.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Ardışık adres mektup birleştirme bölgelerine sahip olduğumuz için normalde iki adres mektup birleştirme gerçekleştirmemiz gerekir.
    // Ancak, veri köküne sahip tek bir adres mektup birleştirme kaynağı birden çok bölgeyi doldurabilir
    // kök, karşılık gelen adlara/sütun adlarına sahip tablolar içeriyorsa.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Giriş dizisi tarafından belirlenen adlarla ardışık adres mektup birleştirme bölgelerini içeren bir belge oluşturun,
/// çalışanların veri tablosu için.
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
/// Uygulamanızda bir "veri varlığı" sınıfı örneği.
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
/// "veri" nesnelerinizi içeren bir yazılı koleksiyon örneği.
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
/// Birçok alt veri kaynağını kaydedebilen ve içerebilen bir adres mektup birleştirmeye doğrudan aktarılabilen veri kaynağı kökü.
/// Bu kaynakların tümü IMailMergeDataSource'u uygulamalıdır ve bir adla kaydedilir ve ayırt edilir
/// ilgili verileri okuyacak bir adres mektup birleştirme bölgesine karşılık gelir.
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
/// Özel adres mektup birleştirme veri kaynağı.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
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
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle adres mektup birleştirme yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words, her veri alanı için bir değer almak için bu yöntemi çağırır.
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
                // Belirtmek için Aspose.Words adres mektup birleştirme motoruna "false" döndür
                // bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Alt veri kaynakları, iç içe adres mektup birleştirmeleri içindir.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Ayrıca bakınız

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot)
* class [MailMerge](../../mailmerge)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Bir DataSet'ten adres mektup birleştirme bölgeleri olan bir belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSet | DataSet | Adres mektup birleştirme alanlarına eklenecek verileri içeren Veri Kümesi. |

### Notlar

Belgedeki bir veya daha fazla tablodan tekrarlanabilir mail birleştirme bölgelerine adres mektup birleştirme gerçekleştirmek için bu yöntemi kullanın. Belge içindeki adres mektup birleştirme bölgeleri, ilgili tablolardaki kayıtları barındırmak için dinamik olarak büyüyecektir.

DataSet içindeki her tablonun bir adı olmalıdır.

Belgede, Veri Kümesi'ndeki tablolara başvuran adlarla tanımlanmış adres mektup birleştirme bölgeleri olmalıdır.

Belgede bir adres-mektup birleştirme bölgesi belirtmek için, adres-mektup birleştirme bölgesinin başlangıcını ve sonunu işaretlemek için iki adres-mektup birleştirme alanı eklemeniz gerekir.

Adres mektup birleştirme bölgesinde bulunan tüm belge içeriği, DataTable'daki her kayıt için otomatik olarak yinelenecektir.

Adres mektup birleştirme bölgesinin başlangıcını işaretlemek için TableStart:MyTable, adında bir MERGEFIELD ekleyin; burada MyTable, DataSet'inizdeki tablo adlarından birine karşılık gelir.

Adres mektup birleştirme bölgesinin sonunu işaretlemek için TableEnd:MyTable adında başka bir MERGEFIELD ekleyin.

Word'de bir MERGEFIELD eklemek için Ekle/Alan komutunu kullanın ve MergeField'i seçin, ardından alanın adını yazın.

TableStart ve TableEnd alanları belgenizde aynı bölümün içinde olmalıdır.

Bir tablo içinde kullanılıyorsa, TableStart ve TableEnd tablodaki aynı satırın içinde olmalıdır.

Bir belgedeki adres mektup birleştirme bölgeleri iyi biçimlendirilmiş olmalıdır (her zaman aynı tablo adına sahip bir çift eşleşen TableStart ve TableEnd birleştirme alanı olması gerekir).

### Örnekler

İki birleştirme bölgesi ve iki veri tablosuyla iç içe adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
[Test]
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalde, MERGEFIELD'ler adres mektup birleştirme veri kaynağının bir sütununun adını içerir.
    // Bunun yerine, adres mektup birleştirme bölgesini başlatmak/sonlandırmak için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
    // Her bölge, önek iki nokta üst üste işaretinden hemen sonraki dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Bu MERGEFIELD, "Müşteriler" tablosunun adres mektup birleştirme bölgesinin içindedir.
    // Adres mektup birleştirmeyi gerçekleştirdiğimizde, bu alan "Müşteriler" adlı bir veri kaynağındaki satırlardan veri alacaktır.
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // İkinci bir iç bölgeden değerler içerecek bir tablo için sütun başlıkları oluşturun.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // "Siparişler" adlı bir tablo için dış bölge içinde ikinci bir adres mektup birleştirme bölgesi oluşturun.
    // "Siparişler" tablosunun "CustomerID" sütunundaki "Customers" tablosuyla çoktan bir ilişkisi vardır.
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // İç bölgeyi ve ardından dış bölgeyi sonlandırın. Adres mektup birleştirme bölgesinin açılması ve kapanması
    // bir tablonun aynı satırında gerçekleşir.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Gerekli adlara ve ilişkilere sahip iki tabloyu içeren bir veri kümesi oluşturun.
    // Dış birleştirme bölgesinin "Müşteriler" tablosunun her satırı için her birleştirme belgesi, adres mektup birleştirmesini "Siparişler" tablosunda gerçekleştirir.
    // Her bir birleştirme belgesi, "CustomerID" sütun değerleri geçerli "Customers" tablo satırıyla eşleşen ikinci tablonun tüm satırlarını görüntüler.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// "Customers" ve "Siparişler" adlı iki veri tablosuna sahip, "CustomerID" sütununda bire çok ilişkisi olan bir veri kümesi oluşturur.
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

### Ayrıca bakınız

* class [MailMerge](../../mailmerge)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Adres mektup birleştirme bölgeleri olan bir DataTable'dan belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataTable | DataTable | Adres mektup birleştirme işlemi için veri kaynağı. Tablo must sahip olmalıdır **Tablo ismi** özellik kümesi. |

### Notlar

Belgenin, ile eşleşen adla tanımlanmış bir adres mektup birleştirme bölgesine sahip olması gerekir. **DataTable.TableName**.

Belgede tanımlanmış başka adres mektup birleştirme bölgeleri varsa, bunlar olduğu gibi bırakılır. Bu, birkaç adres mektup birleştirme işleminin gerçekleştirilmesine olanak tanır.

### Örnekler

Adres mektup birleştirme sırasında hücrelerin nasıl biçimlendirileceğini gösterir.

```csharp
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");

/// <summary>
/// Tablo satırlarını, tek/çift satırlarda iki renk arasında geçiş yapmak için adres mektup birleştirme gerçekleştiğinde biçimlendirir.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Adres mektup birleştirme verileri bir MERGEFIELD ile birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Bu, ilk sütunda olduğumuz için doğrudur, bu da yeni bir satıra taşındığımız anlamına gelir.
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
        // Hiçbir şey yapma.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Geçirilen sayının paritesini döndüren Visual Basic otomatik taşıma için gerekli işlev.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Adres mektup birleştirme veri kaynağı oluşturur.
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

Tek bir belgede iki ayrı adres mektup birleştirme yürütmek için bölgelerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İki tablodan veri alırken tek bir belge üzerinde iki ardışık adres mektup birleştirme yapmak istiyorsak
// birbiri ile herhangi bir şekilde ilişkili olan adres mektup birleştirmelerini bölgelere ayırabiliriz.
// Normalde, MERGEFIELD'ler adres mektup birleştirme veri kaynağının bir sütununun adını içerir.
// Bunun yerine, adres mektup birleştirme bölgesini başlatmak/sonlandırmak için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
// Her bölge, önek iki nokta üst üste işaretinden hemen sonraki dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
// Bu bölgeler ilgisiz veriler için ayrıdır, hiyerarşik veriler için yuvalanabilirler.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Her iki MERGEFIELD aynı sütun adına atıfta bulunur, ancak her birinin değerleri farklı veri tablolarından gelecektir.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Birbiriyle alakasız iki veri tablosu oluşturun.
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

// Tablo başına bir adres mektup birleştirme çalıştırmamız gerekecek. İlk adres mektup birleştirme MERGEFIELD'leri dolduracak
// "Şehirler" aralığında, "Meyve" alanını boş bırakırken.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Veri görünümü kullanırken "Meyve" tablosu için ikinci bir birleştirme çalıştırın
// birleştirmeden önce "Ad" sütunundaki satırları artan düzende sıralamak için.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Ayrıca bakınız

* class [MailMerge](../../mailmerge)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Adres-mektup birleştirme bölgeleri olan bir DataView'den belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataView | DataView | Adres mektup birleştirme işlemi için veri kaynağı. kaynak tablosu  **Veri görünümü** sahip olmalı **Tablo ismi** özellik kümesi. |

### Notlar

Bu yöntem, verileri bir **Veri tablosu** ancak then adres mektup birleştirmeden önce bir filtre veya sıralama uygulamanız gerekir.

Belgenin, ile eşleşen adla tanımlanmış bir adres mektup birleştirme bölgesine sahip olması gerekir. **DataView.Table.TableName**.

Belgede tanımlanmış başka adres mektup birleştirme bölgeleri varsa, bunlar olduğu gibi bırakılır. Bu, birkaç adres mektup birleştirme işleminin gerçekleştirilmesine olanak tanır.

### Örnekler

Tek bir belgede iki ayrı adres mektup birleştirme yürütmek için bölgelerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İki tablodan veri alırken tek bir belge üzerinde iki ardışık adres mektup birleştirme yapmak istiyorsak
// birbiri ile herhangi bir şekilde ilişkili olan adres mektup birleştirmelerini bölgelere ayırabiliriz.
// Normalde, MERGEFIELD'ler adres mektup birleştirme veri kaynağının bir sütununun adını içerir.
// Bunun yerine, adres mektup birleştirme bölgesini başlatmak/sonlandırmak için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
// Her bölge, önek iki nokta üst üste işaretinden hemen sonraki dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
// Bu bölgeler ilgisiz veriler için ayrıdır, hiyerarşik veriler için yuvalanabilirler.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Her iki MERGEFIELD aynı sütun adına atıfta bulunur, ancak her birinin değerleri farklı veri tablolarından gelecektir.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Birbiriyle alakasız iki veri tablosu oluşturun.
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

// Tablo başına bir adres mektup birleştirme çalıştırmamız gerekecek. İlk adres mektup birleştirme MERGEFIELD'leri dolduracak
// "Şehirler" aralığında, "Meyve" alanını boş bırakırken.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Veri görünümü kullanırken "Meyve" tablosu için ikinci bir birleştirme çalıştırın
// birleştirmeden önce "Ad" sütunundaki satırları artan düzende sıralamak için.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Ayrıca bakınız

* class [MailMerge](../../mailmerge)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Adres mektup birleştirme bölgeleriyle IDataReader'dan belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataReader | IDataReader | OleDbDataReader veya SqlDataReader gibi adres mektup birleştirme için veri kayıtlarının kaynağı. |
| tableName | String | Belgedeki doldurulacak adres mektup birleştirme bölgesinin adı. |

### Notlar

Geçebilirsin **SqlDataOkuyucu** veya **OleDbDataOkuyucu** her ikisi de uygulandığı için parametre olarak this yöntemine nesne **IDataOkuyucu** arayüz.

### Örnekler

Veritabanı BLOB alanında saklanan görüntülerin bir rapora nasıl ekleneceğini gösterir.

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

        // Tüm kayıtları bir kerede okuyan bir modda olması gereken veri okuyucuyu açın.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hiçbir şey yapma.
    }

    /// <summary>
    /// Adres mektup birleştirme, belgede adında "Image:" etiketi olan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Ayrıca bakınız

* class [MailMerge](../../mailmerge)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
