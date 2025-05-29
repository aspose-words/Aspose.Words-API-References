---
title: IMailMergeDataSourceRoot.GetDataSource
linktitle: GetDataSource
articleTitle: GetDataSource
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words 解锁无缝邮件合并！探索 IMailMergeDataSourceRoot GetDataSource 方法如何增强您的文档自动化流程。
type: docs
weight: 10
url: /zh/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Aspose.Words 邮件合并引擎在遇到顶级邮件合并区域的开头时调用此方法。

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableName | String | 模板文档中指定的邮件合并区域的名称。不区分大小写。 |

### 返回值

提供对指定表的数据记录的访问的数据源对象。

## 评论

当 Aspose.Words 邮件合并引擎用数据填充文档并遇到 MERGEFIELD TableStart:TableName, 时，它会调用`GetDataSource`在此对象上。您的实现需要返回一个新的数据源对象。 Aspose.Words 将使用返回的数据源来填充邮件合并区域。

如果不存在具有指定名称的数据源（表），则您的实现应该返回`无效的`.

## 例子

从具有主从数据的自定义数据源执行邮件合并。

```csharp
public void CustomDataSourceRoot()
{
    // 创建一个包含两个邮件合并区域的文档，分别名为“华盛顿”和“西雅图”。
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // 为邮件合并创建两个数据源。
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // 在数据源根中按名称注册我们的数据源。
    // 如果我们要在与区域邮件合并中使用此数据源根，
    // 每个源的注册名称必须与邮件合并源文档中现有邮件合并区域的名称相匹配。
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // 由于我们有连续的邮件合并区域，因此我们通常必须执行两次邮件合并。
    // 但是，一个具有数据根的邮件合并源可以填充多个区域
    // 如果根包含具有相应名称/列名的表。
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// 创建一个包含连续邮件合并区域的文档，其名称由输入数组指定，
/// 用于员工数据表。
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
/// 您的应用程序中“数据实体”类的示例。
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
/// 包含“数据”对象的类型集合的示例。
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
/// 可以直接传递到邮件合并中的数据源根，该邮件合并可以注册并包含许多子数据源。
/// 这些源都必须实现 IMailMergeDataSource，并通过名称进行注册和区分
/// 对应于将读取相应数据的邮件合并区域。
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
/// 自定义邮件合并数据源。
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// 移动到集合中的下一个记录的标准实现。
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
    /// 数据源的名称。仅在执行可重复区域的邮件合并时由 Aspose.Words 使用。
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words 调用此方法来获取每个数据字段的值。
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
                // 返回“false”给 Aspose.Words 邮件合并引擎以表示
                // 我们找不到具有此名称的字段。
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// 子数据源用于嵌套邮件合并。
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### 也可以看看

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
