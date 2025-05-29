---
title: IMailMergeDataSource.GetValue
linktitle: GetValue
articleTitle: GetValue
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة IMailMergeDataSource GetValue، واسترجع قيم الحقول بسهولة، أو احصل على قيمة خاطئة في حال عدم العثور عليها. بسّط إدارة بياناتك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.mailmerging/imailmergedatasource/getvalue/
---
## IMailMergeDataSource.GetValue method

يعيد قيمة لاسم الحقل المحدد أو`خطأ شنيع` إذا لم يتم العثور على الحقل.

```csharp
public bool GetValue(string fieldName, out object fieldValue)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldName | String | اسم حقل البيانات. |
| fieldValue | Object& | إرجاع قيمة الحقل. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على القيمة.

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
