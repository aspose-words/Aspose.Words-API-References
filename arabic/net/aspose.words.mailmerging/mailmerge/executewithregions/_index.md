---
title: ExecuteWithRegions
second_title: Aspose.Words لمراجع .NET API
description: يقوم بإجراء دمج بريد من مصدر بيانات مخصص بمناطق دمج البريد.
type: docs
weight: 200
url: /ar/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

يقوم بإجراء دمج بريد من مصدر بيانات مخصص بمناطق دمج البريد.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | كائن يقوم بتنفيذ واجهة مصدر بيانات دمج المراسلات المخصصة. |

### ملاحظات

استخدم هذه الطريقة لتعبئة حقول دمج المراسلات في المستند بقيم من أي مصدر بيانات مخصص مثل ملف XML أو مجموعات كائنات الأعمال. تحتاج إلى كتابة your class الخاص الذي يقوم بتنفيذ ملف[`IMailMergeDataSource`](../../imailmergedatasource/) واجهه المستخدم.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)خطأ ، يعني أنك لا تحتاج إلى توافق مع لغة من اليمين إلى اليسار (مثل العربية أو العبرية).

### أمثلة

يوضح كيفية استخدام مناطق دمج البريد لتنفيذ عملية دمج بريد متداخلة.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // عادةً ، تحتوي MERGEFIELDs على اسم عمود مصدر بيانات دمج المراسلات.
    // بدلاً من ذلك ، يمكننا استخدام البادئات "TableStart:" و "TableEnd:" لبدء / إنهاء منطقة دمج المراسلات.
    // ستنتمي كل منطقة إلى جدول باسم يطابق السلسلة مباشرة بعد نقطتي البادئة.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // هذه MERGEFIELDs موجودة داخل منطقة دمج المراسلات لجدول "العملاء".
    // عند تنفيذ دمج البريد ، سيتلقى هذا الحقل البيانات من الصفوف في مصدر البيانات المسمى "العملاء".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // إنشاء منطقة دمج بريد ثانية داخل المنطقة الخارجية لمصدر بيانات يسمى "الطلبات".
    // تحتوي إدخالات بيانات "الطلبات" على علاقة رأس برأس مع مصدر بيانات "العملاء".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // إنشاء بيانات ذات صلة بأسماء تطابق تلك الخاصة بمناطق دمج البريد الخاصة بنا.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // لدمج المراسلات من مصدر بياناتك ، يجب أن نلفها في كائن يقوم بتنفيذ واجهة IMailMergeDataSource.
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
/// مثال على مجموعة مكتوبة تحتوي على كائنات "البيانات" الخاصة بك.
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
/// مثال على فئة "كيان البيانات" التابعة في تطبيقك.
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
/// مصدر بيانات مخصص لدمج البريد تقوم بتنفيذه للسماح لـ Aspose.Words 
/// لدمج البيانات من كائنات العميل في مستندات Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // عندما نقوم بتهيئة مصدر البيانات ، يجب أن يكون موضعه قبل السجل الأول.
        mRecordIndex = -1;
    }

    /// <summary>
    /// اسم مصدر البيانات. تستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع المناطق القابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words تستدعي هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // إرجاع "خطأ" إلى محرك دمج المراسلات Aspose.Words للإشارة
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
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

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        switch (tableName)
        {
            // احصل على مصدر البيانات التابع ، الذي يتطابق اسمه مع منطقة دمج المراسلات التي تستخدم أعمدتها.
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

        // عندما نقوم بتهيئة مصدر البيانات ، يجب أن يكون موضعه قبل السجل الأول.
        mRecordIndex = -1;
    }

    /// <summary>
    /// اسم مصدر البيانات. تستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع المناطق القابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words تستدعي هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // إرجاع "خطأ" إلى محرك دمج المراسلات Aspose.Words للإشارة
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
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

    /// <summary>
    /// Return null لأننا لا نملك أي عناصر فرعية لهذا النوع من الكائنات.
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
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

يقوم بإجراء دمج بريد من مصدر بيانات مخصص بمناطق دمج البريد.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | كائن يقوم بتطبيق واجهة جذر مصدر بيانات دمج المراسلات المخصصة. |

### ملاحظات

استخدم هذه الطريقة لتعبئة حقول دمج المراسلات في المستند بقيم من أي مصدر بيانات مخصص مثل ملف XML أو مجموعات كائنات الأعمال. تحتاج إلى كتابة class الخاصة بك التي تنفذ ملف[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) و[`IMailMergeDataSource`](../../imailmergedatasource/) واجهات.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)خطأ ، يعني أنك لا تحتاج إلى توافق مع لغة من اليمين إلى اليسار (مثل العربية أو العبرية).

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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

تنفيذ دمج البريد من DataSet في مستند مع مناطق دمج المراسلات.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSet | DataSet | DataSet التي تحتوي على بيانات ليتم إدراجها في حقول دمج المراسلات. |

### ملاحظات

استخدم هذه الطريقة لإجراء دمج البريد من جدول واحد أو أكثر في مناطق دمج mail قابلة للتكرار في المستند. ستنمو مناطق دمج المراسلات داخل المستند ديناميكيًا لتلائم السجلات الموجودة في الجداول المقابلة.

يجب أن يكون لكل جدول في DataSet اسم.

يجب أن يحتوي المستند على مناطق دمج مراسلات محددة بأسماء تشير إلىجدول في DataSet.

لتحديد منطقة دمج المراسلات في المستند ، تحتاج إلى إدراج حقلي دمج المراسلات لوضع علامة على بداية منطقة دمج المراسلات ونهايتها.

سيتم تكرار محتوى المستند بالكامل المتضمن داخل منطقة دمج المراسلات تلقائيًا لكل سجل في DataTable.

لوضع علامة على بداية منطقة دمج المراسلات ، أدخل MERGEFIELD بالاسم TableStart: MyTable، حيث يتوافق MyTable مع أحد أسماء الجدول في DataSet.

لوضع علامة على نهاية منطقة دمج المراسلات ، أدخل MERGEFIELD آخر باسم TableEnd: MyTable.

لإدراج MERGEFIELD في Word ، استخدم الأمر Insert / Field وحدد MergeField ثم اكتب اسم الحقل.

يجب أن يكون حقلا TableStart و TableEnd داخل نفس القسم في المستند.

إذا تم استخدامه داخل جدول ، يجب أن يكون TableStart و TableEnd داخل نفس الصف في الجدول.

يجب أن يتم تشكيل مناطق دمج المراسلات في مستند بشكل جيد (يجب أن يكون هناك دائمًا زوج من حقول دمج Match TableStart و TableEnd بنفس اسم الجدول).

### أمثلة

يوضح كيفية تنفيذ دمج بريد متداخل مع منطقتي دمج وجدولين بيانات.

```csharp
[Test]
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // عادةً ، تحتوي MERGEFIELDs على اسم عمود مصدر بيانات دمج المراسلات.
    // بدلاً من ذلك ، يمكننا استخدام البادئات "TableStart:" و "TableEnd:" لبدء / إنهاء منطقة دمج المراسلات.
    // ستنتمي كل منطقة إلى جدول باسم يطابق السلسلة مباشرة بعد نقطتي البادئة.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // هذا MERGEFIELD داخل منطقة دمج المراسلات لجدول "العملاء".
    // عند تنفيذ دمج البريد ، سيتلقى هذا الحقل البيانات من الصفوف في مصدر البيانات المسمى "العملاء".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // إنشاء رؤوس أعمدة لجدول يحتوي على قيم من منطقة داخلية ثانية.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // إنشاء منطقة دمج بريد ثانية داخل المنطقة الخارجية لجدول يسمى "الطلبات".
    // يحتوي جدول "الطلبات" على علاقة رأس برأس مع جدول "العملاء" في عمود "معرف العميل".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // قم بإنهاء المنطقة الداخلية ، ثم قم بإنهاء المنطقة الخارجية. يجب أن يتم فتح وإغلاق منطقة دمج المراسلات
    // يحدث في نفس الصف من الجدول.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // إنشاء مجموعة بيانات تحتوي على الجدولين بالأسماء والعلاقات المطلوبة.
    // سينفذ كل مستند دمج لكل صف من جدول "العملاء" الخاص بمنطقة الدمج الخارجية عملية دمج المراسلات الخاصة به في جدول "الطلبات".
    // سيعرض كل مستند دمج كافة صفوف الجدول الأخير الذي تطابق قيم عمود "معرف العميل" الخاص به صف جدول "العملاء" الحالي.
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// يُنشئ مجموعة بيانات تحتوي على جدولي بيانات باسم "العملاء" و "الطلبات" ، بعلاقة رأس بأطراف في عمود "معرف العميل".
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
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

تنفيذ دمج المراسلات من DataTable في المستند مع مناطق دمج المراسلات.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataTable | DataTable | مصدر البيانات لعملية دمج المراسلات. الجدول must له **اسم الطاولة** مجموعة الممتلكات. |

### ملاحظات

يجب أن يحتوي المستند على منطقة دمج مراسلات محددة باسم يطابق  **DataTable.TableName**.

إذا كانت هناك مناطق دمج مراسلات أخرى محددة في المستند ، فإنها تُترك كما هي . وهذا يسمح بإجراء العديد من عمليات دمج المراسلات.

### أمثلة

يوضح كيفية تنسيق الخلايا أثناء دمج البريد.

```csharp
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");

/// <summary>
/// تنسيقات صفوف الجدول عندما يحدث دمج المراسلات للتبديل بين لونين على الصفوف الفردية / الزوجية.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// يتم الاستدعاء عندما يقوم دمج المراسلات بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // هذا صحيح أننا في العمود الأول ، مما يعني أننا انتقلنا إلى صف جديد.
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
        // لا تفعل شيئا.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// الوظيفة المطلوبة لإجراء Visual Basic autoporting الذي يُرجع تماثل الرقم الذي تم تمريره.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// ينشئ مصدر بيانات لدمج المراسلات.
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

يوضح كيفية استخدام المناطق لتنفيذ عمليتي دمج بريد منفصلين في مستند واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا إجراء عمليتي دمج متتاليتين للبريد في مستند واحد أثناء أخذ البيانات من جدولين
// المرتبطة ببعضها البعض بأي شكل من الأشكال ، يمكننا فصل عمليات دمج البريد مع المناطق.
// عادةً ، تحتوي MERGEFIELDs على اسم عمود مصدر بيانات دمج المراسلات.
// بدلاً من ذلك ، يمكننا استخدام البادئات "TableStart:" و "TableEnd:" لبدء / إنهاء منطقة دمج المراسلات.
// ستنتمي كل منطقة إلى جدول باسم يطابق السلسلة مباشرة بعد نقطتي البادئة.
// هذه المناطق منفصلة عن البيانات غير المرتبطة ، بينما يمكن أن تكون متداخلة للبيانات الهرمية.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// يشير كلا المخططين MERGEFIELD إلى نفس اسم العمود ، ولكن ستأتي قيم كل منهما من جداول بيانات مختلفة.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// إنشاء جدولين غير مرتبطين بالبيانات.
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

// سنحتاج إلى تشغيل دمج بريد واحد لكل جدول. سيتم ملء دمج المراسلات الأول في MERGEFIELDs
// في نطاق "المدن" مع ترك الحقول في نطاق "الفاكهة" شاغرة.
doc.MailMerge.ExecuteWithRegions(tableCities);

// قم بإجراء عملية دمج ثانية لجدول "الفاكهة" ، أثناء استخدام عرض البيانات
// لفرز الصفوف بترتيب تصاعدي على عمود "الاسم" قبل الدمج.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

تنفيذ دمج المراسلات من DataView في المستند مع مناطق دمج المراسلات.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataView | DataView | مصدر البيانات لعملية دمج المراسلات. مصدر table لملف **عرض البيانات** يجب أن يكون لها **اسم الطاولة** مجموعة الممتلكات. |

### ملاحظات

هذه الطريقة مفيدة إذا قمت باسترداد البيانات إلى ملف **جدول البيانات** ولكن then تحتاج إلى تطبيق عامل تصفية أو فرز قبل دمج المراسلات.

يجب أن يحتوي المستند على منطقة دمج مراسلات محددة باسم يطابق  **DataView.Table.TableName**.

إذا كانت هناك مناطق دمج مراسلات أخرى محددة في المستند ، فإنها تُترك كما هي . وهذا يسمح بإجراء العديد من عمليات دمج المراسلات.

### أمثلة

يوضح كيفية استخدام المناطق لتنفيذ عمليتي دمج بريد منفصلين في مستند واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا إجراء عمليتي دمج متتاليتين للبريد في مستند واحد أثناء أخذ البيانات من جدولين
// المرتبطة ببعضها البعض بأي شكل من الأشكال ، يمكننا فصل عمليات دمج البريد مع المناطق.
// عادةً ، تحتوي MERGEFIELDs على اسم عمود مصدر بيانات دمج المراسلات.
// بدلاً من ذلك ، يمكننا استخدام البادئات "TableStart:" و "TableEnd:" لبدء / إنهاء منطقة دمج المراسلات.
// ستنتمي كل منطقة إلى جدول باسم يطابق السلسلة مباشرة بعد نقطتي البادئة.
// هذه المناطق منفصلة عن البيانات غير المرتبطة ، بينما يمكن أن تكون متداخلة للبيانات الهرمية.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// يشير كلا المخططين MERGEFIELD إلى نفس اسم العمود ، ولكن ستأتي قيم كل منهما من جداول بيانات مختلفة.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// إنشاء جدولين غير مرتبطين بالبيانات.
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

// سنحتاج إلى تشغيل دمج بريد واحد لكل جدول. سيتم ملء دمج المراسلات الأول في MERGEFIELDs
// في نطاق "المدن" مع ترك الحقول في نطاق "الفاكهة" شاغرة.
doc.MailMerge.ExecuteWithRegions(tableCities);

// قم بإجراء عملية دمج ثانية لجدول "الفاكهة" ، أثناء استخدام عرض البيانات
// لفرز الصفوف بترتيب تصاعدي على عمود "الاسم" قبل الدمج.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

تنفيذ دمج المراسلات من IDataReader في المستند باستخدام مناطق دمج المراسلات.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataReader | IDataReader | مصدر سجلات البيانات لدمج المراسلات مثل OleDbDataReader أو SqlDataReader. |
| tableName | String | اسم منطقة دمج المراسلات في المستند المراد تعبئتها. |

### ملاحظات

يمكنك تمرير **SqlDataReader** أو **OleDbDataReader** الكائن في طريقة this كمعامل لأن كلاهما تم تنفيذهما **إداتاريدر** واجهه المستخدم.

### أمثلة

يوضح كيفية إدراج الصور المخزنة في حقل BLOB لقاعدة البيانات في تقرير.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // افتح قارئ البيانات ، الذي يجب أن يكون في وضع يقرأ جميع السجلات مرة واحدة.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // لا تفعل شيئا.
    }

    /// <summary>
    /// يتم استدعاء هذا عندما يواجه دمج المراسلات MERGEFIELD في المستند بعلامة "صورة:" في اسمه.
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
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
