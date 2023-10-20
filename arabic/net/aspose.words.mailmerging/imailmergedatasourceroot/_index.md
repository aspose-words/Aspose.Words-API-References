---
title: IMailMergeDataSourceRoot Interface
linktitle: IMailMergeDataSourceRoot
articleTitle: IMailMergeDataSourceRoot
second_title: Aspose.Words لـ .NET
description: Aspose.Words.MailMerging.IMailMergeDataSourceRoot واجهه المستخدم. قم بتنفيذ هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص مع البيانات الرئيسية التفصيلية في C#.
type: docs
weight: 3820
url: /ar/net/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface

قم بتنفيذ هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص مع البيانات الرئيسية التفصيلية.

```csharp
public interface IMailMergeDataSourceRoot
```

## طُرق

| اسم | وصف |
| --- | --- |
| [GetDataSource](../../aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/)(*string*) | يقوم محرك دمج المراسلات Aspose.Words باستدعاء هذه الطريقة عندما يواجه بداية منطقة دمج المراسلات ذات المستوى الأعلى. |

## أمثلة

تنفيذ دمج البريد من مصدر بيانات مخصص مع بيانات رئيسية وتفصيلية.

```csharp
public void CustomDataSourceRoot()
{
    // قم بإنشاء مستند يحتوي على منطقتين لدمج البريد باسم "واشنطن" و"سياتل".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // إنشاء مصدرين للبيانات لدمج المراسلات.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // قم بتسجيل مصادر البيانات الخاصة بنا بالاسم في جذر مصدر البيانات.
    // إذا كنا على وشك استخدام جذر مصدر البيانات هذا في دمج البريد مع المناطق،
    // يجب أن يتطابق الاسم المسجل لكل مصدر مع اسم منطقة دمج المراسلات الموجودة في مستند مصدر دمج المراسلات.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // بما أن لدينا مناطق متتالية لدمج البريد، فعادةً ما يتعين علينا إجراء عمليتين لدمج البريد.
    // ومع ذلك، يمكن لمصدر دمج مراسلات واحد ذو جذر بيانات ملء مناطق متعددة
    // إذا كان الجذر يحتوي على جداول ذات أسماء/أسماء أعمدة مقابلة.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// أنشئ مستندًا يحتوي على مناطق متتالية لدمج البريد، بأسماء محددة بواسطة مصفوفة الإدخال،
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
/// مثال لفئة "كيان البيانات" في التطبيق الخاص بك.
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
/// مثال لمجموعة مكتوبة تحتوي على كائنات "البيانات" الخاصة بك.
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
/// جذر مصدر البيانات الذي يمكن تمريره مباشرة إلى عملية دمج البريد التي يمكنها التسجيل وتحتوي على العديد من مصادر البيانات الفرعية.
/// يجب أن تقوم جميع هذه المصادر بتنفيذ IMailMergeDataSource، وأن يتم تسجيلها وتمييزها باسم
/// الذي يتوافق مع منطقة دمج البريد التي ستقرأ البيانات المعنية.
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
/// مصدر بيانات دمج البريد المخصص.
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
    /// اسم مصدر البيانات. يُستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع المناطق القابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// يستدعي Aspose.Words هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // قم بإرجاع "خطأ" إلى محرك دمج البريد Aspose.Words للدلالة
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// مصادر البيانات الفرعية مخصصة لدمج البريد المتداخل.
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
