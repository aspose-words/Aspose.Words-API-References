---
title: IMailMergeDataSource.TableName
second_title: Aspose.Words لمراجع .NET API
description: IMailMergeDataSource ملكية. إرجاع اسم مصدر البيانات.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/imailmergedatasource/tablename/
---
## IMailMergeDataSource.TableName property

إرجاع اسم مصدر البيانات.

```csharp
public string TableName { get; }
```

### قيمة الإرجاع

اسم مصدر البيانات. سلسلة فارغة إذا لم يكن لمصدر البيانات اسم.

### ملاحظات

إذا كنت تنفذ[`IMailMergeDataSource`](../)، قم بإرجاع اسم مصدر data من هذه الخاصية.

يستخدم Aspose.Words هذا الاسم لمطابقة اسم منطقة دمج المراسلات المحدد في مستند النموذج. المقارنة بين اسم مصدر البيانات و اسم منطقة دمج المراسلات ليست حساسة لحالة الأحرف.

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

* interface [IMailMergeDataSource](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../imailmergedatasource/)
* المجسم [Aspose.Words](../../../)


