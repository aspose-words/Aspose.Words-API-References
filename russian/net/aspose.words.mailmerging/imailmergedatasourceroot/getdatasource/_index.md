---
title: GetDataSource
second_title: Справочник по API Aspose.Words для .NET
description: Механизм слияния почты Aspose.Words вызывает этот метод когда обнаруживает начало области слияния почты верхнего уровня.
type: docs
weight: 10
url: /ru/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало области слияния почты верхнего уровня.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | String | Имя региона слияния, как указано в шаблоне документа. Без учета регистра. |

### Возвращаемое значение

Объект источника данных, который предоставит доступ к записям данных указанной таблицы.

### Примечания

Когда механизмы слияния Aspose.Words заполняют документ data и встречает MERGEFIELD TableStart:TableName, он вызывает`GetDataSource`для этого объекта. Ваша реализация должна вернуть новый объект источника данных. Aspose.Words будет использовать возвращенный источник данных для заполнения области слияния.

Если источник данных (таблица) с указанным именем не существует, ваша реализация должна вернуть` null` .

### Примеры

Выполняет слияние почты из пользовательского источника данных с основными и подробными данными.

```csharp
public void CustomDataSourceRoot()
{
     // Создайте документ с двумя регионами слияния с именами «Вашингтон» и «Сиэтл».
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

     // Создадим два источника данных для слияния.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

     // Регистрируем наши источники данных по имени в корне источника данных.
    // Если мы собираемся использовать этот корень источника данных в слиянии почты с регионами, 
     // зарегистрированное имя каждого источника должно соответствовать имени существующей области слияния в исходном документе слияния.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

     // Поскольку у нас есть последовательные регионы слияния, обычно нам приходится выполнять два слияния.
     // Однако один источник слияния с корнем данных может заполнить несколько регионов
     // если в корне есть таблицы с соответствующими именами/именами столбцов.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
 /// Создать документ, содержащий последовательные области слияния с именами, указанными во входном массиве, 
 /// для таблицы данных сотрудников.
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
 /// Пример класса "объект данных" в вашем приложении.
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
 /// Пример типизированной коллекции, содержащей ваши объекты "данные".
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
 /// Корень источника данных, который можно передать непосредственно в слияние, которое может регистрироваться и содержать множество дочерних источников данных.
/// Все эти источники должны реализовывать IMailMergeDataSource, они зарегистрированы и отличаются именем
 /// что соответствует области слияния почты, которая будет считывать соответствующие данные.
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
 /// Пользовательский источник данных слияния почты.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
     /// Стандартная реализация перехода к следующей записи в коллекции.
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
     /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяемыми регионами.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
     /// Aspose.Words вызывает этот метод, чтобы получить значение для каждого поля данных.
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
                 // Возвращаем "false" механизму слияния почты Aspose.Words для signify
                 // что мы не смогли найти поле с таким именем.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
     /// Дочерние источники данных предназначены для вложенных слияний почты.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Смотрите также

* interface [IMailMergeDataSource](../../imailmergedatasource)
* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot)
* namespace [Aspose.Words.MailMerging](../../imailmergedatasourceroot)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
