---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل طريقة IMailMergeDataSource GetChildDataSource على تعزيز دمج البريد في Aspose.Words من خلال إدارة المناطق المتداخلة بسلاسة.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

يستدعي محرك دمج البريد Aspose.Words هذه الطريقة عندما يواجه بداية منطقة دمج بريد متداخلة.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableName | String | اسم منطقة دمج البريد كما هو محدد في مستند القالب. لا يُفرق بين الأحرف الكبيرة والصغيرة. |

### قيمة الإرجاع

كائن مصدر بيانات يوفر إمكانية الوصول إلى سجلات البيانات الخاصة بالجدول المحدد.

## ملاحظات

عندما تقوم محركات دمج البريد Aspose.Words بملء منطقة دمج البريد بالبيانات وتواجه بداية منطقة دمج البريد nested في شكل MERGEFIELD TableStart:TableName، فإنها تستدعي`GetChildDataSource` على كائن مصدر البيانات current . يحتاج تطبيقك إلى إرجاع كائن مصدر بيانات جديد يتيح الوصول إلى سجلات child للسجل الرئيسي الحالي. سيستخدم Aspose.Words مصدر البيانات المُعاد لملء منطقة دمج البريد المتداخلة.

فيما يلي القواعد التي يجب اتباعها عند تنفيذ`GetChildDataSource` يجب أن يتبع.

إذا كان الجدول الذي يمثله كائن مصدر البيانات هذا يحتوي على جدول فرعي (تفاصيل) مرتبط بالاسم المحدد، ، فيجب أن يقوم التنفيذ الخاص بك بإرجاع جدول جديد[`IMailMergeDataSource`](../) كائن يوفر الوصول إلى السجلات الفرعية للسجل الحالي. مثال على ذلك علاقة الطلبات / تفاصيل الطلب. لنفترض أن السجل الحالي[`IMailMergeDataSource`](../) object يمثل جدول الطلبات، ويحتوي على سجل طلب حالي. بعد ذلك، يواجه Aspose.Words "MERGEFIELD TableStart:OrderDetails" في المستند، ويستدعي`GetChildDataSource` . تحتاج إلى إنشاء وإرجاع[`IMailMergeDataSource`](../) كائن الذي سيسمح لـ Aspose.Words بالوصول إلى سجل OrderDetails للطلب الحالي.

إذا لم يكن لكائن مصدر البيانات هذا علاقة بالجدول الذي يحمل الاسم المحدد، فستحتاج إلى إرجاع a[`IMailMergeDataSource`](../)الكائن الذي سيوفر الوصول إلى جميع سجلات الجدول المحدد.

إذا لم يكن هناك جدول يحمل الاسم المحدد، فيجب أن يقوم التنفيذ الخاص بك بإرجاع`باطل` .

## أمثلة

يوضح كيفية تنفيذ دمج البريد مع مصدر البيانات في شكل كائن مخصص.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // لاستخدام كائن مخصص كمصدر بيانات، يجب عليه تنفيذ واجهة IMailMergeDataSource.
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
 /// مصدر بيانات دمج البريد المخصص الذي تقوم بتنفيذه للسماح لـ Aspose.Words
/// لدمج البيانات من كائنات العميل الخاصة بك في مستندات Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
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
        get { return "Customer"; }
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

* interface [IMailMergeDataSource](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
