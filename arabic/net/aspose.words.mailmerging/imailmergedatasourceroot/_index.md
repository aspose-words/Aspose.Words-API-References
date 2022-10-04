---
title: IMailMergeDataSourceRoot
second_title: Aspose.Words لمراجع .NET API
description: قم بتطبيق هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص ببيانات رئيسيةتفصيلية.
type: docs
weight: 3600
url: /ar/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

قم بتطبيق هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص ببيانات رئيسية-تفصيلية.

```csharp
public interface IMailMergeDataSourceRoot
```

## طُرق

| اسم | وصف |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(string) | يستدعي محرك دمج المراسلات Aspose.Words هذه الطريقة عندما يواجه بداية منطقة دمج بريد عالية المستوى . |

### أمثلة

ينفذ دمج البريد من مصدر بيانات مخصص مع بيانات رئيسية-تفصيلية.

```csharp
public void CustomDataSourceRoot()
{
    // إنشاء مستند بمنطقتين لدمج المراسلات باسم "واشنطن" و "سياتل".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // إنشاء مصدري بيانات لدمج البريد.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // سجل مصادر البيانات لدينا بالاسم في جذر مصدر البيانات.
    // إذا كنا على وشك استخدام جذر مصدر البيانات هذا في دمج البريد مع المناطق ،
    // يجب أن يتطابق الاسم المسجل لكل مصدر مع اسم منطقة دمج المراسلات الموجودة في مستند مصدر دمج المراسلات.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // نظرًا لوجود مناطق متتالية لدمج البريد ، فسنضطر عادةً إلى إجراء عمليتي دمج بريد.
    // ومع ذلك ، يمكن لمصدر دمج بريد واحد مع جذر بيانات ملء مناطق متعددة
    // إذا كان الجذر يحتوي على جداول بأسماء / أسماء أعمدة مقابلة.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// قم بإنشاء مستند يحتوي على مناطق دمج مراسلات متتالية ، بأسماء محددة بواسطة صفيف الإدخال ،
/// لجدول بيانات الموظفين.
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
/// مثال على فئة "كيان البيانات" في تطبيقك.
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
/// مثال على مجموعة مكتوبة تحتوي على كائنات "البيانات" الخاصة بك.
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
/// جذر مصدر البيانات الذي يمكن تمريره مباشرةً إلى دمج المراسلات والذي يمكنه تسجيل العديد من مصادر البيانات الفرعية واحتوائها.
/// يجب أن تقوم جميع هذه المصادر بتنفيذ IMailMergeDataSource ، وأن يتم تسجيلها وتمييزها عن طريق الاسم
/// الذي يتوافق مع منطقة دمج المراسلات التي ستقرأ البيانات المعنية.
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
/// مصدر بيانات دمج المراسلات المخصص.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// تطبيق قياسي للانتقال إلى السجل التالي في المجموعة.
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
    /// اسم مصدر البيانات. تستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع المناطق القابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words تستدعي هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // إرجاع "خطأ" إلى محرك دمج المراسلات Aspose.Words للإشارة
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// مصادر البيانات الفرعية مخصصة لعمليات دمج البريد المتداخلة.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
