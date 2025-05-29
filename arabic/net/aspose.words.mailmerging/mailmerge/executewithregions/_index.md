---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words لـ .NET
description: قم بتبسيط عملية إنشاء المستندات لديك باستخدام طريقة MailMerge ExecuteWithRegions، مما يتيح لك دمج البريد بكفاءة من مصادر البيانات والمناطق المخصصة.
type: docs
weight: 200
url: /ar/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

يقوم بتنفيذ دمج البريد من مصدر بيانات مخصص مع مناطق دمج البريد.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | كائن ينفذ واجهة مصدر بيانات دمج البريد المخصصة. |

## ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من أي مصدر بيانات مخصص، مثل ملف XML أو مجموعات من كائنات الأعمال. ستحتاج إلى كتابة فئة خاصة بك تُطبّق [`IMailMergeDataSource`](../../imailmergedatasource/) واجهة.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) يكون`خطأ شنيع`, وهذا يعني أنك لا تحتاج إلى توافق اللغة من اليمين إلى اليسار (مثل العربية أو العبرية).

## أمثلة

يوضح كيفية استخدام مناطق دمج البريد لتنفيذ دمج بريد متداخل.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // عادةً، تحتوي حقول الدمج على اسم عمود في مصدر بيانات دمج البريد.
    // بدلاً من ذلك، يمكننا استخدام البادئات "TableStart:" و"TableEnd:" لبدء/إنهاء منطقة دمج البريد.
    // ستنتمي كل منطقة إلى جدول يحمل اسمًا يتطابق مع السلسلة الموجودة مباشرة بعد علامة النقطتين في البادئة.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    //توجد حقول الدمج هذه داخل منطقة دمج البريد في جدول "العملاء".
    // عندما نقوم بتنفيذ عملية دمج البريد، سيستقبل هذا الحقل البيانات من الصفوف الموجودة في مصدر البيانات المسمى "العملاء".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // قم بإنشاء منطقة دمج بريد ثانية داخل المنطقة الخارجية لمصدر بيانات يسمى "الطلبات".
    // تحتوي إدخالات بيانات "الطلبات" على علاقة متعددة إلى واحدة مع مصدر بيانات "العملاء".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // قم بإنشاء بيانات ذات صلة بأسماء تتطابق مع أسماء مناطق دمج البريد لدينا.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // لدمج البريد من مصدر البيانات الخاص بك، يجب علينا تغليفه في كائن ينفذ واجهة IMailMergeDataSource.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// مثال على فئة "كيان البيانات" في تطبيقك.
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
/// مثال لمجموعة مكتوبة تحتوي على كائنات "البيانات" الخاصة بك.
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
/// مثال لفئة "كيان البيانات" الفرعية في تطبيقك.
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
 /// مصدر بيانات دمج البريد المخصص الذي تقوم بتنفيذه للسماح لـ Aspose.Words
/// لدمج البيانات من كائنات العميل الخاصة بك في مستندات Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // عندما نقوم بتهيئة مصدر البيانات، يجب أن يكون موضعه قبل السجل الأول.
        mRecordIndex = -1;
    }

    /// <summary>
    /// اسم مصدر البيانات. يُستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع مناطق قابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// تستدعي Aspose.Words هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // قم بإرجاع "false" إلى محرك دمج البريد Aspose.Words للإشارة إلى
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
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

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        switch (tableName)
        {
            // احصل على مصدر البيانات الفرعي، الذي يتطابق اسمه مع منطقة دمج البريد التي تستخدم أعمدته.
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

        // عندما نقوم بتهيئة مصدر البيانات، يجب أن يكون موضعه قبل السجل الأول.
        mRecordIndex = -1;
    }

    /// <summary>
    /// اسم مصدر البيانات. يُستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع مناطق قابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// تستدعي Aspose.Words هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // قم بإرجاع "false" إلى محرك دمج البريد Aspose.Words للإشارة إلى
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
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

    /// <summary>
    /// إرجاع null لأننا لا نملك أي عناصر فرعية لهذا النوع من الكائنات.
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

### أنظر أيضا

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

يقوم بتنفيذ دمج البريد من مصدر بيانات مخصص مع مناطق دمج البريد.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | كائن ينفذ واجهة جذر مصدر بيانات دمج البريد المخصصة. |

## ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من أي مصدر بيانات مخصص، مثل ملف XML أو مجموعات من كائنات الأعمال. ستحتاج إلى كتابة فئاتك الخاصة التي تُطبّق[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) و[`IMailMergeDataSource`](../../imailmergedatasource/) الواجهات.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) يكون`خطأ شنيع`, وهذا يعني أنك لا تحتاج إلى توافق اللغة من اليمين إلى اليسار (مثل العربية أو العبرية).

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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

يقوم بدمج البريد من**مجموعة البيانات** في مستند يحتوي على مناطق دمج البريد.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSet | DataSet | **مجموعة البيانات** الذي يحتوي على البيانات التي سيتم إدراجها في حقول دمج البريد. |

## ملاحظات

استخدم هذه الطريقة لدمج البريد من جدول واحد أو أكثر في مناطق دمج mail قابلة للتكرار في المستند. ستنمو مناطق دمج البريد داخل المستند ديناميكيًا لاستيعاب السجلات في الجداول المقابلة.

كل طاولة في**مجموعة البيانات** يجب أن يكون له اسم.

يجب أن تحتوي الوثيقة على مناطق دمج بريد محددة بأسماء تشير إلى tables في**مجموعة البيانات**.

لتحديد منطقة دمج البريد في المستند، يجب عليك إدراج حقلين لدمج البريد لتمييز بداية ونهاية منطقة دمج البريد.

سيتم تكرار كل محتوى المستند المضمن داخل منطقة دمج البريد تلقائيًا لكل سجل في**جدول البيانات**.

لتحديد بداية منطقة دمج البريد، أدخل MERGEFIELD باسم TableStart:MyTable, حيث يتوافق MyTable مع أحد أسماء الجداول في**مجموعة البيانات**.

لتحديد نهاية منطقة دمج البريد، أدخل MERGEFIELD آخر باسم TableEnd:MyTable.

لإدراج MERGEFIELD في Word استخدم الأمر Insert/Field وحدد MergeField ثم اكتب اسم الحقل .

ال**بدء تشغيل الجدول** و**نهاية الجدول** يجب أن تكون الحقول داخل نفس القسم في مستندك.

إذا تم استخدامه داخل جدول،**بدء تشغيل الجدول** و**نهاية الجدول** يجب أن يكون داخل نفس الصف في الجدول.

يجب أن تكون مناطق دمج البريد في المستند مُشكَّلة بشكل جيد (يجب أن يكون هناك دائمًا زوج من المطابقة **بدء تشغيل الجدول** و**نهاية الجدول** دمج الحقول التي لها نفس اسم الجدول).

## أمثلة

يوضح كيفية تنفيذ دمج البريد المتداخل مع منطقتي دمج وجدولين بيانات.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // عادةً، تحتوي حقول الدمج على اسم عمود في مصدر بيانات دمج البريد.
    // بدلاً من ذلك، يمكننا استخدام البادئات "TableStart:" و"TableEnd:" لبدء/إنهاء منطقة دمج البريد.
    // ستنتمي كل منطقة إلى جدول يحمل اسمًا يتطابق مع السلسلة الموجودة مباشرة بعد علامة النقطتين في البادئة.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // يقع هذا MERGEFIELD داخل منطقة دمج البريد في جدول "العملاء".
    // عندما نقوم بتنفيذ عملية دمج البريد، سيستقبل هذا الحقل البيانات من الصفوف الموجودة في مصدر البيانات المسمى "العملاء".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // إنشاء رؤوس الأعمدة للجدول الذي سيحتوي على قيم من منطقة داخلية ثانية.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // قم بإنشاء منطقة دمج بريد ثانية داخل المنطقة الخارجية لجدول يسمى "الطلبات".
    // يحتوي جدول "الطلبات" على علاقة متعددة إلى واحدة مع جدول "العملاء" في عمود "معرف العميل".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // أنهِ المنطقة الداخلية، ثم أنهِ المنطقة الخارجية. يجب أن يكون فتح وإغلاق منطقة دمج البريد
    // يحدث في نفس الصف من الجدول.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // قم بإنشاء مجموعة بيانات تحتوي على الجدولين بالأسماء والعلاقات المطلوبة.
    // سوف يقوم كل مستند دمج لكل صف من جدول "العملاء" في منطقة الدمج الخارجية بتنفيذ عملية دمج البريد الخاصة به على جدول "الطلبات".
    // سوف يعرض كل مستند دمج جميع صفوف الجدول الأخير الذي تتطابق قيم عمود "CustomerID" فيه مع صف جدول "Customers" الحالي.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// إنشاء مجموعة بيانات تحتوي على جدولين للبيانات باسم "العملاء" و"الطلبات"، مع علاقة واحد إلى متعدد في عمود "معرف العميل".
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

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

يقوم بدمج البريد من**جدول البيانات** في المستند مع مناطق دمج البريد.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataTable | DataTable | مصدر بيانات عملية دمج البريد. يجب أن يحتوي الجدول علىTableName مجموعة الخصائص. |

## ملاحظات

يجب أن تحتوي الوثيقة على منطقة دمج بريد محددة باسم يطابق TableName.

إذا كانت هناك مناطق دمج بريد أخرى محددة في المستند، فسيتم تركها كما هي. يسمح هذا بإجراء العديد من عمليات دمج البريد.

## أمثلة

يوضح كيفية تنسيق الخلايا أثناء دمج البريد.

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
/// تنسيق صفوف الجدول أثناء عملية دمج البريد للتبديل بين لونين في الصفوف الفردية/الزوجية.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// يتم استدعاؤها عندما يقوم دمج البريد بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // هذا صحيح إذا كنا في العمود الأول، مما يعني أننا انتقلنا إلى صف جديد.
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
        //لا تفعل شيئا.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// هناك حاجة إلى وظيفة للتنفيذ التلقائي في Visual Basic والتي تقوم بإرجاع التكافؤ للرقم المرسل.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// إنشاء مصدر بيانات دمج البريد.
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

يوضح كيفية استخدام المناطق لتنفيذ دمجين بريديين منفصلين في مستند واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا تنفيذ دمجين متتاليين للبريد على مستند واحد أثناء أخذ البيانات من جدولين
//إذا كانت عمليات الدمج البريدية مرتبطة ببعضها البعض بأي شكل من الأشكال، فيمكننا فصل عمليات الدمج البريدية حسب المناطق.
// عادةً، تحتوي حقول الدمج على اسم عمود في مصدر بيانات دمج البريد.
// بدلاً من ذلك، يمكننا استخدام البادئات "TableStart:" و"TableEnd:" لبدء/إنهاء منطقة دمج البريد.
// ستنتمي كل منطقة إلى جدول يحمل اسمًا يتطابق مع السلسلة الموجودة مباشرة بعد علامة النقطتين في البادئة.
// تكون هذه المناطق منفصلة للبيانات غير ذات الصلة، في حين يمكن أن تكون متداخلة للبيانات الهرمية.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// يشير كلا MERGEFIELDs إلى نفس اسم العمود، ولكن القيم لكل منهما ستأتي من جداول بيانات مختلفة.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// إنشاء جدولين بيانات غير مرتبطين.
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

// سنحتاج إلى تشغيل دمج بريد واحد لكل جدول. سيملأ الدمج الأول حقول الدمج.
// في نطاق "المدن" مع ترك الحقول في نطاق "الفواكه" غير مملوءة.
doc.MailMerge.ExecuteWithRegions(tableCities);

// قم بتشغيل دمج ثانٍ لجدول "Fruit"، أثناء استخدام عرض البيانات
// لفرز الصفوف بترتيب تصاعدي في عمود "الاسم" قبل الدمج.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

يقوم بدمج البريد من**عرض البيانات** في المستند مع مناطق دمج البريد.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataView | DataView | مصدر بيانات عملية دمج البريد. جدول المصدر لـ**عرض البيانات** يجب أن يكون لها**اسم الجدول** مجموعة الخصائص. |

## ملاحظات

هذه الطريقة مفيدة إذا كنت ترغب في استرداد البيانات في**جدول البيانات** ولكن بعد ذلك، يجب تطبيق عامل تصفية أو فرز قبل دمج البريد.

يجب أن تحتوي الوثيقة على منطقة دمج بريد محددة باسم يطابق **DataView.Table.TableName**.

إذا كانت هناك مناطق دمج بريد أخرى محددة في المستند، فسيتم تركها كما هي. يسمح هذا بإجراء العديد من عمليات دمج البريد.

## أمثلة

يوضح كيفية استخدام المناطق لتنفيذ دمجين بريديين منفصلين في مستند واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا تنفيذ دمجين متتاليين للبريد على مستند واحد أثناء أخذ البيانات من جدولين
//إذا كانت عمليات الدمج البريدية مرتبطة ببعضها البعض بأي شكل من الأشكال، فيمكننا فصل عمليات الدمج البريدية حسب المناطق.
// عادةً، تحتوي حقول الدمج على اسم عمود في مصدر بيانات دمج البريد.
// بدلاً من ذلك، يمكننا استخدام البادئات "TableStart:" و"TableEnd:" لبدء/إنهاء منطقة دمج البريد.
// ستنتمي كل منطقة إلى جدول يحمل اسمًا يتطابق مع السلسلة الموجودة مباشرة بعد علامة النقطتين في البادئة.
// تكون هذه المناطق منفصلة للبيانات غير ذات الصلة، في حين يمكن أن تكون متداخلة للبيانات الهرمية.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// يشير كلا MERGEFIELDs إلى نفس اسم العمود، ولكن القيم لكل منهما ستأتي من جداول بيانات مختلفة.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// إنشاء جدولين بيانات غير مرتبطين.
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

// سنحتاج إلى تشغيل دمج بريد واحد لكل جدول. سيملأ الدمج الأول حقول الدمج.
// في نطاق "المدن" مع ترك الحقول في نطاق "الفواكه" غير مملوءة.
doc.MailMerge.ExecuteWithRegions(tableCities);

// قم بتشغيل دمج ثانٍ لجدول "Fruit"، أثناء استخدام عرض البيانات
// لفرز الصفوف بترتيب تصاعدي في عمود "الاسم" قبل الدمج.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

يقوم بدمج البريد من**قارئ بيانات الهوية** في المستند مع مناطق دمج البريد.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataReader | IDataReader | مصدر سجلات البيانات لدمج البريد مثل**قارئ بيانات OleDb** أو**قارئ بيانات SQL**. |
| tableName | String | اسم منطقة دمج البريد في المستند الذي سيتم ملؤه. |

## ملاحظات

يمكنك المرور**قارئ بيانات SQL** أو**قارئ بيانات OleDb** الكائن في طريقة this كمعلمة لأن كلاهما تم تنفيذه**قارئ بيانات الهوية** واجهة.

## أمثلة

يوضح كيفية إدراج الصور المخزنة في حقل BLOB بقاعدة البيانات في تقرير.

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

        // افتح قارئ البيانات، والذي يجب أن يكون في وضع يقرأ جميع السجلات مرة واحدة.
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
        //لا تفعل شيئا.
    }

    /// <summary>
    /// يتم استدعاء هذا عندما يواجه دمج البريد MERGEFIELD في المستند مع علامة "Image:" في اسمه.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
