---
title: GetDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words adres mektup birleştirme motoru bir üst düzey adres mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Aspose.Words adres mektup birleştirme motoru, bir üst düzey adres mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableName | String | Şablon belgesinde belirtilen adres mektup birleştirme bölgesinin adı. Büyük/küçük harfe duyarsız. |

### Geri dönüş değeri

Belirtilen tablonun veri kayıtlarına erişim sağlayacak bir veri kaynağı nesnesi.

### Notlar

Aspose.Words adres mektup birleştirme motorları bir belgeyi verilerle doldurduğunda ve MERGEFIELD TableStart:TableName, ile karşılaştığında, onu çağırır`GetDataSource` bu nesne üzerinde. Uygulamanızın yeni bir veri kaynağı nesnesi döndürmesi gerekiyor. Aspose.Words, adres mektup birleştirme bölgesini doldurmak için döndürülen veri kaynağını kullanacak.

Belirtilen ada sahip bir veri kaynağı (tablo) yoksa, uygulamanız geri dönmelidir`hükümsüz` .

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

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* ad alanı [Aspose.Words.MailMerging](../../imailmergedatasourceroot/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
