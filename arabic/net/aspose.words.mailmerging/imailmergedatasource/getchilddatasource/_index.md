---
title: GetChildDataSource
second_title: Aspose.Words لمراجع .NET API
description: يستدعي محرك دمج المراسلات Aspose.Words هذه الطريقة عندما يواجه بداية منطقة دمج بريد متداخلة.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

يستدعي محرك دمج المراسلات Aspose.Words هذه الطريقة عندما يواجه بداية منطقة دمج بريد متداخلة.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableName | String | اسم منطقة دمج المراسلات كما هو محدد في مستند القالب. حالة الأحرف. |

### قيمة الإرجاع

عنصر مصدر بيانات سيوفر الوصول إلى سجلات البيانات في الجدول المحدد.

### ملاحظات

عندما تملأ محركات دمج المراسلات Aspose.Words منطقة دمج بريد بالبيانات وتواجه بداية منطقة دمج بريد متداخلة في شكل MERGEFIELD TableStart: TableName ، تستدعي`GetChildDataSource` على كائن مصدر البيانات current . يحتاج التنفيذ الخاص بك إلى إرجاع كائن مصدر بيانات جديد يوفر الوصول إلى سجلات child للسجل الأصل الحالي. سوف تستخدم كلمات Aspose.Words مصدر البيانات الذي تم إرجاعه لملء منطقة دمج البريد المتداخلة.

فيما يلي القواعد التي يتم تنفيذها`GetChildDataSource` يجب أن تتبع ._ x000d_

إذا كان الجدول الذي يمثله كائن مصدر البيانات هذا يحتوي على جدول فرعي (تفصيلي) مرتبط بالاسم المحدد ، فحينئذٍ يحتاج التنفيذ إلى إرجاع عنصر جديد[`IMailMergeDataSource`](../../imailmergedatasource) الذي سيوفر access إلى السجلات التابعة للسجل الحالي. مثال على ذلك هو علاقة الطلبات / تفاصيل الطلب. لنفترض أن التيار[`IMailMergeDataSource`](../../imailmergedatasource) يمثل object جدول الطلبات وله سجل أوامر حالي. بعد ذلك ، يواجه Aspose.Words "MERGEFIELD TableStart: OrderDetails" في المستند ويستدعى`GetChildDataSource` . تحتاج إلى إنشاء وإرجاع ملف[`IMailMergeDataSource`](../../imailmergedatasource) كائن سيسمح لـ Aspose.Words بالوصول إلى سجل OrderDetails للطلب الحالي.

إذا لم يكن لكائن مصدر البيانات هذا علاقة بالجدول بالاسم المحدد ، فأنت بحاجة إلى return a[`IMailMergeDataSource`](../../imailmergedatasource)الذي سيوفر الوصول إلى جميع سجلات الجدول المحدد.

في حالة عدم وجود جدول بالاسم المحدد ، يجب أن يعود التنفيذ`لا شيء` .

### أمثلة

يوضح كيفية تنفيذ دمج المراسلات مع مصدر بيانات في شكل كائن مخصص.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    // لاستخدام كائن مخصص كمصدر بيانات ، يجب أن يقوم بتنفيذ واجهة IMailMergeDataSource. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
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
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
/// مصدر بيانات مخصص لدمج البريد تقوم بتنفيذه للسماح لـ Aspose.Words 
/// لدمج البيانات من كائنات العميل في مستندات Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
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
        get { return "Customer"; }
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
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### أنظر أيضا

* interface [IMailMergeDataSource](../../imailmergedatasource)
* مساحة الاسم [Aspose.Words.MailMerging](../../imailmergedatasource)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
