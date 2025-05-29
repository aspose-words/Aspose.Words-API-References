---
title: IMailMergeDataSourceRoot Interface
linktitle: IMailMergeDataSourceRoot
articleTitle: IMailMergeDataSourceRoot
second_title: .NET için Aspose.Words
description: Aspose.Words.MailMerging.IMailMergeDataSourceRoot ile güçlü e-posta birleştirmenin kilidini açın. Ana-ayrıntılı veri işleme için özel veri kaynaklarını sorunsuz bir şekilde entegre edin.
type: docs
weight: 4510
url: /tr/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

Bu arayüzü, ana-ayrıntılı veriler içeren özel bir veri kaynağından posta birleştirmeye izin verecek şekilde uygulayın.

```csharp
public interface IMailMergeDataSourceRoot
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(*string*) | Aspose.Words posta birleştirme motoru, en üst düzey bir posta birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır. |

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
