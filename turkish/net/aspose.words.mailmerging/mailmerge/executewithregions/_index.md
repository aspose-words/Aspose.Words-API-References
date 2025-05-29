---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: .NET için Aspose.Words
description: MailMerge ExecuteWithRegions yöntemiyle belge oluşturma işleminizi kolaylaştırın; özel veri kaynaklarından ve bölgelerden etkili posta birleştirme işlemleri gerçekleştirin.
type: docs
weight: 200
url: /tr/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

Posta birleştirme bölgeleriyle özel bir veri kaynağından posta birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Özel posta birleştirme veri kaynağı arayüzünü uygulayan bir nesne. |

## Notlar

Bu yöntemi, belgedeki posta birleştirme alanlarını XML dosyası veya iş nesneleri koleksiyonları gibi herhangi bir özel veri kaynağından gelen değerlerle doldurmak için kullanın. Bunu uygulayan kendi sınıfınızı yazmanız gerekir.[`IMailMergeDataSource`](../../imailmergedatasource/) arayüz.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) dır`YANLIŞ`, yani Sağdan Sola dil (örneğin Arapça veya İbranice) uyumluluğuna ihtiyacınız yok.

## Örnekler

İç içe geçmiş bir posta birleştirmeyi gerçekleştirmek için posta birleştirme bölgelerinin nasıl kullanılacağını gösterir.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalde, MERGEFIELD'ler bir posta birleştirme veri kaynağının bir sütununun adını içerir.
    // Bunun yerine, bir posta birleştirme bölgesini başlatmak/bitirmek için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
    // Her bölge, önekin iki nokta üst üste işaretinden hemen sonra gelen dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Bu MERGEFIELD'lar "Customers" tablosunun posta birleştirme bölgesinin içindedir.
    // Posta birleştirme işlemini gerçekleştirdiğimizde bu alan "Müşteriler" adlı veri kaynağındaki satırlardan veri alacaktır.
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // "Siparişler" adlı bir veri kaynağı için dış bölgenin içinde ikinci bir posta birleştirme bölgesi oluşturun.
    // "Siparişler" veri girişleri, "Müşteriler" veri kaynağıyla çoktan bire ilişkiye sahiptir.
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Birleştirme bölgelerimizdeki adlarla eşleşen ilişkili verileri oluşturun.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Veri kaynağınızdan posta birleştirme yapmak için, onu IMailMergeDataSource arayüzünü uygulayan bir nesneye sarmamız gerekir.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Uygulamanızdaki "veri varlığı" sınıfının bir örneği.
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
/// "Veri" nesnelerinizi içeren türlendirilmiş bir koleksiyonun örneği.
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
/// Uygulamanızdaki bir alt "veri varlığı" sınıfının örneği.
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
 /// Aspose.Words'e izin vermek için uyguladığınız özel bir posta birleştirme veri kaynağı
/// Müşteri nesnelerinizdeki verileri Microsoft Word belgelerine birleştirmek için.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // Veri kaynağını başlattığımızda, konumunun ilk kayıttan önce olması gerekir.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle posta birleştirme işlemi yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words her veri alanı için bir değer almak amacıyla bu metodu çağırır.
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
                // Aspose.Words posta birleştirme motoruna "false" değerini döndürerek belirtin
                // Bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Bir koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
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
            // Sütunlarını kullanan posta birleştirme bölgesiyle eşleşen adı olan alt veri kaynağını alın.
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

        // Veri kaynağını başlattığımızda, konumunun ilk kayıttan önce olması gerekir.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle posta birleştirme işlemi yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words her veri alanı için bir değer almak amacıyla bu metodu çağırır.
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
                // Aspose.Words posta birleştirme motoruna "false" değerini döndürerek belirtin
                // Bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Bir koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    /// <summary>
    /// Bu tür nesneler için herhangi bir alt öğemiz olmadığından null döndürüyoruz.
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

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

Posta birleştirme bölgeleriyle özel bir veri kaynağından posta birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Özel posta birleştirme veri kaynağı kök arayüzünü uygulayan bir nesne. |

## Notlar

Bu yöntemi, belgedeki posta birleştirme alanlarını XML dosyası veya iş nesneleri koleksiyonları gibi herhangi bir özel veri kaynağından gelen değerlerle doldurmak için kullanın. Aşağıdakileri uygulayan kendi classes 'nizi yazmanız gerekir:[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) Ve[`IMailMergeDataSource`](../../imailmergedatasource/) arayüzler.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) dır`YANLIŞ`, yani Sağdan Sola dil (örneğin Arapça veya İbranice) uyumluluğuna ihtiyacınız yok.

## Örnekler

Özel bir veri kaynağından ana-ayrıntı verileriyle posta birleştirme işlemini gerçekleştirir.

```csharp
public void CustomDataSourceRoot()
{
    // "Washington" ve "Seattle" adında iki birleştirme bölgesi içeren bir belge oluşturun.
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Posta birleştirme için iki veri kaynağı oluşturun.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Veri kaynaklarımızı isme göre bir veri kaynağı köküne kaydedelim.
    // Bu veri kaynağı kökünü bölgelerle bir posta birleştirme işleminde kullanacaksak,
    // her kaynağın kayıtlı adı, posta birleştirme kaynak belgesindeki mevcut bir posta birleştirme bölgesinin adıyla eşleşmelidir.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Ardışık posta birleştirme bölgelerimiz olduğundan, normalde iki posta birleştirme gerçekleştirmemiz gerekir.
    // Ancak, veri kökü olan bir posta birleştirme kaynağı birden fazla bölgeyi doldurabilir
    // eğer kök dizin, karşılık gelen adlara/sütun adlarına sahip tablolar içeriyorsa.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Giriş dizisi tarafından belirtilen adlara sahip ardışık posta birleştirme bölgelerini içeren bir belge oluşturun,
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
/// Uygulamanızdaki "veri varlığı" sınıfının bir örneği.
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
/// "Veri" nesnelerinizi içeren türlendirilmiş bir koleksiyonun örneği.
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
/// Bir posta birleştirme işlemine doğrudan geçirilebilen ve birçok alt veri kaynağını kaydedebilen ve içerebilen veri kaynağı kökü.
/// Bu kaynakların tümü IMailMergeDataSource'u uygulamalı ve bir adla kaydedilmeli ve farklılaştırılmalıdır
/// ilgili verileri okuyacak bir posta birleştirme bölgesine karşılık gelir.
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
/// Özel posta birleştirme veri kaynağı.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Bir koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
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
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle posta birleştirme işlemi yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words her veri alanı için bir değer almak amacıyla bu metodu çağırır.
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
                // Aspose.Words posta birleştirme motoruna "false" değerini döndürerek belirtin
                // Bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Alt veri kaynakları iç içe geçmiş posta birleştirmeleri içindir.
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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

Bir e-posta birleştirme işlemini gerçekleştirir**Veri Seti** posta birleştirme bölgelerine sahip bir belgeye.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSet | DataSet | **Veri Seti** Posta birleştirme alanlarına eklenecek verileri içeren. |

## Notlar

Bu yöntemi, bir veya daha fazla tablodan belgedeki tekrarlanabilir mail birleştirme bölgelerine posta birleştirme gerçekleştirmek için kullanın. Belge içindeki posta birleştirme bölgeleri, karşılık gelen tablolardaki kayıtları barındırmak için dinamik olarak büyüyecektir.

Her masa**Veri Seti** bir ismi olmalı.

Belgede tables 'ye atıfta bulunan adlarla tanımlanmış posta birleştirme bölgeleri bulunmalıdır.**Veri Seti**.

Belgede bir posta birleştirme bölgesi belirtmek için, posta birleştirme bölgesinin başlangıcını ve sonunu işaretlemek üzere iki posta birleştirme alanı eklemeniz gerekir.

Bir posta birleştirme bölgesi içinde yer alan tüm belge içeriği, bölgedeki her kayıt için otomatik olarak tekrarlanacaktır.**Veri Tablosu**.

Bir posta birleştirme bölgesinin başlangıcını işaretlemek için TableStart:MyTable, adlı bir MERGEFIELD ekleyin; burada MyTable, posta birleştirme bölgenizdeki tablo adlarından birine karşılık gelir.**Veri Seti**.

Posta birleştirme bölgesinin sonunu işaretlemek için TableEnd:MyTable adında başka bir MERGEFIELD ekleyin.

Word'de MERGEFIELD eklemek için Ekle/Alan komutunu kullanın ve MergeField'ı seçip alanın adını yazın.

The**TabloBaşlangıcı** Ve**Tablo Sonu** alanlar belgenizde aynı bölümün içerisinde olmalıdır.

Bir tablonun içinde kullanılırsa,**TabloBaşlangıcı** Ve**Tablo Sonu** tabloda aynı satırda olmalıdır.

Bir belgedeki posta birleştirme bölgeleri iyi biçimlendirilmiş olmalıdır (her zaman eşleşen çifti olması gerekir)**TabloBaşlangıcı** Ve**Tablo Sonu** (aynı tablo adına sahip alanları birleştir).

## Örnekler

İki birleştirme bölgesi ve iki veri tablosuyla iç içe geçmiş bir posta birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalde, MERGEFIELD'ler bir posta birleştirme veri kaynağının bir sütununun adını içerir.
    // Bunun yerine, bir posta birleştirme bölgesini başlatmak/bitirmek için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
    // Her bölge, önekin iki nokta üst üste işaretinden hemen sonra gelen dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Bu MERGEFIELD, "Müşteriler" tablosunun posta birleştirme bölgesinin içindedir.
    // Posta birleştirme işlemini gerçekleştirdiğimizde bu alan "Müşteriler" adlı veri kaynağındaki satırlardan veri alacaktır.
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // İkinci bir iç bölgedeki değerleri içerecek bir tablo için sütun başlıkları oluşturun.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // "Siparişler" adlı tablo için dış bölgenin içinde ikinci bir posta birleştirme bölgesi oluşturun.
    // "Siparişler" tablosunun "CustomerID" sütununda "Müşteriler" tablosuyla çoktan bire ilişkisi vardır.
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // İç bölgeyi sonlandırın ve ardından dış bölgeyi sonlandırın. Bir posta birleştirme bölgesinin açılıp kapatılması
    // tablonun aynı satırında gerçekleşir.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Gerekli ad ve ilişkilere sahip iki tabloyu içeren bir veri kümesi oluşturun.
    // Dış birleştirme bölgesindeki "Müşteriler" tablosunun her satırı için her birleştirme belgesi, "Siparişler" tablosunda posta birleştirme işlemini gerçekleştirecektir.
    // Her birleştirme belgesi, "CustomerID" sütun değerleri geçerli "Customers" tablo satırıyla eşleşen son tablonun tüm satırlarını görüntüler.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// "CustomerID" sütununda bire-çok ilişkisi olan "Customers" ve "Orders" adlı iki veri tablosundan oluşan bir veri kümesi oluşturur.
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

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

Bir e-posta birleştirme işlemini gerçekleştirir**Veri Tablosu** posta birleştirme bölgeleriyle belgeye.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataTable | DataTable | Posta birleştirme işlemi için veri kaynağı. must tablosunun kendiTableName özellik seti. |

## Notlar

Belgenin, ile eşleşen bir adla tanımlanmış bir posta birleştirme bölgesi olması gerekirTableName.

Belgede tanımlanmış başka posta birleştirme bölgeleri varsa bunlar olduğu gibi bırakılır. Bu, çeşitli posta birleştirme işlemlerinin gerçekleştirilmesine olanak tanır.

## Örnekler

Posta birleştirme sırasında hücrelerin nasıl biçimlendirileceğini gösterir.

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
/// Tablo satırlarını, tek/çift satırlarda iki renk arasında dönüşümlü olarak gerçekleşen bir posta birleştirme işlemi gibi biçimlendirir.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Bir posta birleştirme işlemi verileri bir MERGEFIELD'a birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Bu, ilk sütunda olduğumuzda geçerlidir, yani yeni bir satıra geçiyoruz.
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
        // Hiçbir şey yapmayın.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Geçirilen sayının paritesini döndüren Visual Basic otomatik aktarımı için gereken fonksiyon.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Bir posta birleştirme veri kaynağı oluşturur.
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

Bir belgede iki ayrı posta birleştirmeyi yürütmek için bölgelerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İki tablodan veri alırken aynı belge üzerinde iki ardışık posta birleştirme işlemi yapmak istiyorsak
// Birbirleriyle herhangi bir şekilde ilişkili olmayan bölgeler için, posta birleştirmelerini bölgelere göre ayırabiliriz.
// Normalde, MERGEFIELD'ler bir posta birleştirme veri kaynağının bir sütununun adını içerir.
// Bunun yerine, bir posta birleştirme bölgesini başlatmak/bitirmek için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
// Her bölge, önekin iki nokta üst üste işaretinden hemen sonra gelen dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
// Bu bölgeler, ilgisiz veriler için ayrıdır, ancak hiyerarşik veriler için iç içe yerleştirilebilir.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Her iki MERGEFIELD da aynı sütun adını ifade eder, ancak her birinin değerleri farklı veri tablolarından gelir.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Birbiriyle ilgisi olmayan iki veri tablosu oluşturun.
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

// Tablo başına bir posta birleştirme çalıştırmamız gerekecek. İlk posta birleştirme MERGEFIELD'leri dolduracak
// "Şehirler" aralığında "Meyve" aralığını boş bırakın.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Veri görünümü kullanırken "Meyve" tablosu için ikinci bir birleştirme çalıştırın
// birleştirmeden önce "Ad" sütununda satırları artan düzende sıralamak için.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

Bir e-posta birleştirme işlemini gerçekleştirir**VeriGörünümü** posta birleştirme bölgeleriyle belgeye.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataView | DataView | Posta birleştirme işlemi için veri kaynağı. Kaynak table **VeriGörünümü** sahip olmalı**TabloAdı** özellik seti. |

## Notlar

Bu yöntem, verileri bir**Veri Tablosu** ancak then birleştirmeden önce bir filtre veya sıralama uygulamanız gerekir.

Belgenin, ile eşleşen bir adla tanımlanmış bir posta birleştirme bölgesi olması gerekir**VeriGörünümü.Tablo.TabloAdı**.

Belgede tanımlanmış başka posta birleştirme bölgeleri varsa bunlar olduğu gibi bırakılır. Bu, çeşitli posta birleştirme işlemlerinin gerçekleştirilmesine olanak tanır.

## Örnekler

Bir belgede iki ayrı posta birleştirmeyi yürütmek için bölgelerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İki tablodan veri alırken aynı belge üzerinde iki ardışık posta birleştirme işlemi yapmak istiyorsak
// Birbirleriyle herhangi bir şekilde ilişkili olmayan bölgeler için, posta birleştirmelerini bölgelere göre ayırabiliriz.
// Normalde, MERGEFIELD'ler bir posta birleştirme veri kaynağının bir sütununun adını içerir.
// Bunun yerine, bir posta birleştirme bölgesini başlatmak/bitirmek için "TableStart:" ve "TableEnd:" öneklerini kullanabiliriz.
// Her bölge, önekin iki nokta üst üste işaretinden hemen sonra gelen dizeyle eşleşen bir ada sahip bir tabloya ait olacaktır.
// Bu bölgeler, ilgisiz veriler için ayrıdır, ancak hiyerarşik veriler için iç içe yerleştirilebilir.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Her iki MERGEFIELD da aynı sütun adını ifade eder, ancak her birinin değerleri farklı veri tablolarından gelir.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Birbiriyle ilgisi olmayan iki veri tablosu oluşturun.
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

// Tablo başına bir posta birleştirme çalıştırmamız gerekecek. İlk posta birleştirme MERGEFIELD'leri dolduracak
// "Şehirler" aralığında "Meyve" aralığını boş bırakın.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Veri görünümü kullanırken "Meyve" tablosu için ikinci bir birleştirme çalıştırın
// birleştirmeden önce "Ad" sütununda satırları artan düzende sıralamak için.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

Posta birleştirme işlemini gerçekleştirir**IDataOkuyucu** posta birleştirme bölgeleriyle belgeye.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataReader | IDataReader | Posta birleştirme için veri kayıtlarının kaynağı:**OleDbVeriOkuyucu** veya**SqlDataOkuyucu**. |
| tableName | String | Doldurulacak belgedeki posta birleştirme bölgesinin adı. |

## Notlar

Geçebilirsin**SqlDataOkuyucu** veya**OleDbVeriOkuyucu** nesneyi this yöntemine parametre olarak eklediler çünkü ikisi de uygulandı**IDataOkuyucu** arayüz.

## Örnekler

Bir veritabanı BLOB alanında saklanan görsellerin bir rapora nasıl ekleneceğini gösterir.

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

        // Tüm kayıtları aynı anda okuyan bir modda olması gereken veri okuyucusunu açın.
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
        // Hiçbir şey yapmayın.
    }

    /// <summary>
    /// Bu, bir posta birleştirme işlemi belgede adında "Image:" etiketi bulunan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
