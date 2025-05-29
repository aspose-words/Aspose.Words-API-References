---
title: IMailMergeDataSourceRoot.GetDataSource
linktitle: GetDataSource
articleTitle: GetDataSource
second_title: Aspose.Words لـ .NET
description: دمج البريد بسلاسة مع Aspose.Words! اكتشف كيف تُحسّن طريقة IMailMergeDataSourceRoot GetDataSource عملية أتمتة مستنداتك.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

يستدعي محرك دمج البريد Aspose.Words هذه الطريقة عندما يواجه بداية منطقة دمج بريد ذات مستوى أعلى.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableName | String | اسم منطقة دمج البريد كما هو محدد في مستند القالب. لا يُفرق بين الأحرف الكبيرة والصغيرة. |

### قيمة الإرجاع

كائن مصدر بيانات يوفر إمكانية الوصول إلى سجلات البيانات الخاصة بالجدول المحدد.

## ملاحظات

عندما تقوم محركات دمج البريد Aspose.Words بملء مستند بالبيانات وتواجه MERGEFIELD TableStart:TableName، فإنها تستدعي`GetDataSource` على هذا الكائن. يحتاج تنفيذك إلى إرجاع كائن مصدر بيانات جديد. سيستخدم Aspose.Words مصدر البيانات المُعاد لملء منطقة دمج البريد.

إذا لم يكن مصدر البيانات (الجدول) بالاسم المحدد موجودًا، فيجب أن يقوم التنفيذ الخاص بك بإرجاع`باطل` .

## أمثلة

يقوم بإجراء دمج البريد من مصدر بيانات مخصص مع بيانات رئيسية وتفصيلية.

```csharp
public void CustomDataSourceRoot()
{
    // قم بإنشاء مستند يحتوي على منطقتين لدمج البريد باسم "واشنطن" و"سياتل".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // إنشاء مصدرين للبيانات لدمج البريد.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // قم بتسجيل مصادر البيانات الخاصة بنا بالاسم في جذر مصدر البيانات.
    // إذا كنا على وشك استخدام جذر مصدر البيانات هذا في دمج البريد مع المناطق،
    // يجب أن يتطابق الاسم المسجل لكل مصدر مع اسم منطقة دمج البريد الموجودة في مستند مصدر دمج البريد.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // نظرًا لأن لدينا مناطق دمج بريد متتالية، فمن الطبيعي أن نضطر إلى تنفيذ دمج بريدين.
    // ومع ذلك، يمكن لمصدر دمج بريد واحد مع جذر بيانات ملء مناطق متعددة
    // إذا كان الجذر يحتوي على جداول ذات أسماء/أسماء أعمدة مقابلة.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// قم بإنشاء مستند يحتوي على مناطق دمج بريد متتالية، مع أسماء محددة بواسطة مجموعة الإدخال،
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
/// جذر مصدر البيانات الذي يمكن تمريره مباشرة إلى دمج البريد الذي يمكنه تسجيل العديد من مصادر البيانات الفرعية واحتواءها.
/// يجب أن تنفذ جميع هذه المصادر IMailMergeDataSource، ويتم تسجيلها وتمييزها باسم
/// والتي تتوافق مع منطقة دمج البريد التي ستقرأ البيانات المعنية.
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
    /// تنفيذ قياسي للانتقال إلى السجل التالي في المجموعة.
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
    /// اسم مصدر البيانات. يُستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع مناطق قابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// تستدعي Aspose.Words هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // قم بإرجاع "false" إلى محرك دمج البريد Aspose.Words للإشارة إلى
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

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
