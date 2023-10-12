---
title: IMailMergeDataSource.MoveNext
second_title: Aspose.Words لمراجع .NET API
description: IMailMergeDataSource طريقة. التقدم إلى السجل التالي في مصدر البيانات.
type: docs
weight: 40
url: /ar/net/aspose.words.mailmerging/imailmergedatasource/movenext/
---
## IMailMergeDataSource.MoveNext method

التقدم إلى السجل التالي في مصدر البيانات.

```csharp
public bool MoveNext()
```

### قيمة الإرجاع

`حقيقي` إذا تم نقله إلى السجل التالي بنجاح؛`خطأ شنيع` إذا وصلت إلى نهاية مصدر البيانات.

### أمثلة

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
* مساحة الاسم [Aspose.Words.MailMerging](../../imailmergedatasource/)
* المجسم [Aspose.Words](../../../)


