---
title: IMailMergeDataSourceRoot Interface
linktitle: IMailMergeDataSourceRoot
articleTitle: IMailMergeDataSourceRoot
second_title: Aspose.Words for .NET
description: Aspose.Words.MailMerging.IMailMergeDataSourceRoot arayüz. Ana ayrıntı verileriyle özel bir veri kaynağından adresmektup birleştirmeye izin vermek için bu arayüzü uygulayın C#'da.
type: docs
weight: 3820
url: /tr/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

Ana ayrıntı verileriyle özel bir veri kaynağından adres-mektup birleştirmeye izin vermek için bu arayüzü uygulayın.

```csharp
public interface IMailMergeDataSourceRoot
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(*string*) | Aspose.Words adres-mektup birleştirme motoru, üst düzey adres-mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır. |

## Örnekler

Ana ayrıntı verileriyle özel bir veri kaynağından adres-mektup birleştirme gerçekleştirir.

```csharp
public void CustomDataSourceRoot()
{
    // "Washington" ve "Seattle" adlı iki adres-mektup birleştirme bölgesine sahip bir belge oluşturun.
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Adres-mektup birleştirme için iki veri kaynağı oluşturun.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Veri kaynaklarımızı bir veri kaynağı köküne ada göre kaydedin.
    // Bu veri kaynağı kökünü bölgelerle adres-mektup birleştirmede kullanmak üzereysek,
    // her kaynağın kayıtlı adı, adres-mektup birleştirme kaynak belgesindeki mevcut adres-mektup birleştirme bölgesinin adıyla eşleşmelidir.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Ardışık adres-mektup birleştirme bölgelerimiz olduğundan normalde iki adres-mektup birleştirme yapmamız gerekir.
    // Ancak, veri köküne sahip bir adres-mektup birleştirme kaynağı birden fazla bölgeyi doldurabilir
    // eğer kök karşılık gelen adlara/sütun adlarına sahip tablolar içeriyorsa.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Giriş dizisi tarafından belirlenen adlarla ardışık adres-mektup birleştirme bölgelerini içeren bir belge oluşturun,
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
/// Uygulamanızdaki "veri varlığı" sınıfına bir örnek.
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
/// "Veri" nesnelerinizi içeren yazılı bir koleksiyon örneği.
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
/// Birçok alt veri kaynağını kaydedebilen ve içerebilen adres-mektup birleştirmeye doğrudan aktarılabilen veri kaynağı kökü.
/// Bu kaynakların tümü IMailMergeDataSource'u uygulamalı ve bir adla kaydedilip farklılaştırılmalıdır
/// ilgili verileri okuyacak adres-mektup birleştirme bölgesine karşılık gelir.
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
/// Özel adres-mektup birleştirme veri kaynağı.
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
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle adres-mektup birleştirme yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words her veri alanı için bir değer elde etmek amacıyla bu yöntemi çağırır.
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
                // Aspose.Words adres-mektup birleştirme motoruna şunu belirtmek için "yanlış" değerini döndürün
                // bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Alt veri kaynakları iç içe adres-mektup birleştirmeler içindir.
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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
