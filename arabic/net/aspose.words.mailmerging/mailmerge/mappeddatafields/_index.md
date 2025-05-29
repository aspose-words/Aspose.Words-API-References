---
title: MailMerge.MappedDataFields
linktitle: MappedDataFields
articleTitle: MappedDataFields
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MailMerge MappedDataFields، وقم بالوصول إلى مجموعة قوية من حقول البيانات المخصصة لتحسين عمليات دمج البريد لديك بسهولة.
type: docs
weight: 50
url: /ar/net/aspose.words.mailmerging/mailmerge/mappeddatafields/
---
## MailMerge.MappedDataFields property

يعيد مجموعة تمثل حقول البيانات المخصصة لعملية دمج البريد.

```csharp
public MappedDataFieldCollection MappedDataFields { get; }
```

## ملاحظات

تتيح لك حقول البيانات المرسومة إجراء رسم بياني تلقائيًا بين أسماء الحقول في مصدر البيانات الخاص بك وأسماء حقول دمج البريد في المستند.

## أمثلة

يوضح كيفية تعيين أعمدة البيانات وحقول الدمج بأسماء مختلفة حتى يتم نقل البيانات بينها أثناء دمج البريد.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // يحتوي الجدول على عمود يسمى "Column2"، ولكن لا توجد حقول MERGEFIELD بهذا الاسم.
    //أيضًا، لدينا MERGEFIELD باسم "Column3"، ولكن مصدر البيانات لا يحتوي على عمود بهذا الاسم.
    // إذا كانت البيانات من "العمود 2" مناسبة لحقل الدمج "العمود 3"،
    // يمكننا تعيين اسم العمود هذا إلى MERGEFIELD في زوج المفتاح/القيمة "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // يمكننا ربط اسم عمود مصدر البيانات باسم MERGEFIELD مثل هذا.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // ربط عمود مصدر البيانات المسمى "Column2" بـ MERGEFIELDs المسمى "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // اسم MERGEFIELD هو "المفتاح" لاسم عمود مصدر البيانات "القيمة".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // الآن إذا قمنا بتشغيل دمج البريد هذا، فإن حقول الدمج "Column3" ستأخذ البيانات من "Column2" في الجدول.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    //يمكننا تكرار العناصر الموجودة في هذه المجموعة.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    //يمكننا أيضًا إزالة العناصر من المجموعة.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// قم بإنشاء مستند يحتوي على حقلين MERGEFIELD، أحدهما لا يحتوي على
/// العمود المقابل في جدول البيانات من الطريقة أدناه.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// قم بإنشاء جدول بيانات يحتوي على عمودين، أحدهما لا يحتوي على
/// MERGEFIELD المقابل في المستند المصدر من الطريقة أعلاه.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### أنظر أيضا

* class [MappedDataFieldCollection](../../mappeddatafieldcollection/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
