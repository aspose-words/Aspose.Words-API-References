---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words لـ .NET
description: IMailMergeDataSource GetChildDataSource طريقة. يقوم محرك دمج المراسلات Aspose.Words باستدعاء هذه الطريقة عندما يواجه بداية منطقة دمج المراسلات المتداخلة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

يقوم محرك دمج المراسلات Aspose.Words باستدعاء هذه الطريقة عندما يواجه بداية منطقة دمج المراسلات المتداخلة.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableName | String | اسم منطقة دمج المراسلات كما هو محدد في مستند القالب. حالة الأحرف. |

### قيمة الإرجاع

كائن مصدر بيانات يوفر الوصول إلى سجلات البيانات الخاصة بالجدول المحدد.

## ملاحظات

عندما تقوم محركات دمج المراسلات Aspose.Words بملء منطقة دمج المراسلات بالبيانات وتواجه بداية منطقة دمج المراسلات المتداخلة في شكل MERGEFIELD TableStart:TableName، فإنها تستدعي`GetChildDataSource` على كائن مصدر البيانات current . يحتاج التنفيذ الخاص بك إلى إرجاع كائن مصدر بيانات جديد يوفر الوصول إلى سجلات Child للسجل الأصلي الحالي. سيستخدم Aspose.Words مصدر البيانات الذي تم إرجاعه لملء منطقة دمج المراسلات المتداخلة.

فيما يلي القواعد التي يتم تنفيذها`GetChildDataSource` يجب أن يتبع.

إذا كان الجدول الذي يمثله كائن مصدر البيانات هذا يحتوي على جدول فرعي (تفاصيل) مرتبط بالاسم المحدد، ، فإن تطبيقك يحتاج إلى إرجاع جدول جديد[`IMailMergeDataSource`](../)الكائن الذي سيوفر إمكانية الوصول إلى السجلات الفرعية للسجل الحالي. مثال على ذلك هو علاقة الطلبات/تفاصيل الطلب. لنفترض أن التيار[`IMailMergeDataSource`](../) يمثل object جدول الطلبات ويحتوي على سجل الطلب الحالي. بعد ذلك، يواجه Aspose.Words "MERGEFIELD TableStart:OrderDetails" في المستند ويستدعيه`GetChildDataSource` . تحتاج إلى إنشاء وإرجاع ملف[`IMailMergeDataSource`](../) كائن الذي سيسمح لـ Aspose.Words بالوصول إلى سجل OrderDetails للطلب الحالي.

إذا لم يكن لكائن مصدر البيانات هذا علاقة بالجدول بالاسم المحدد، فأنت بحاجة إلى إرجاع a[`IMailMergeDataSource`](../) الكائن الذي سيوفر الوصول إلى كافة سجلات الجدول المحدد.

في حالة عدم وجود جدول بالاسم المحدد، يجب أن يعود التنفيذ الخاص بك`باطل` .

## أمثلة

يوضح كيفية تنفيذ دمج البريد مع مصدر بيانات في شكل كائن مخصص.

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
/// مثال لفئة "كيان البيانات" في التطبيق الخاص بك.
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
 /// مصدر بيانات مخصص لدمج البريد تقوم بتنفيذه للسماح بـ Aspose.Words
/// لدمج بيانات البريد من كائنات العميل الخاصة بك في مستندات Microsoft Word.
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
    /// اسم مصدر البيانات. يُستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع المناطق القابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// يستدعي Aspose.Words هذه الطريقة للحصول على قيمة لكل حقل بيانات.
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
                // قم بإرجاع "خطأ" إلى محرك دمج البريد Aspose.Words للدلالة
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

* interface [IMailMergeDataSource](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
