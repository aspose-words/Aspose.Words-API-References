---
title: MappedDataFieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: MappedDataFieldCollection Item ملكية. الحصول على اسم الحقل في مصدر البيانات المقترن بحقل دمج المراسلات المحدد أو تعيينه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/mappeddatafieldcollection/item/
---
## MappedDataFieldCollection indexer

الحصول على اسم الحقل في مصدر البيانات المقترن بحقل دمج المراسلات المحدد أو تعيينه.

```csharp
public string this[string documentFieldName] { get; set; }
```

## أمثلة

يوضح كيفية تعيين أعمدة البيانات وMERGEFIELD بأسماء مختلفة بحيث يتم نقل البيانات فيما بينها أثناء عملية دمج البريد.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // يحتوي الجدول على عمود يسمى "Column2"، لكن لا توجد حقول دمج بهذا الاسم.
    // أيضًا، لدينا حقل MERGEFIELD يُسمى "Column3"، لكن مصدر البيانات لا يحتوي على عمود بهذا الاسم.
    // إذا كانت البيانات من "Column2" مناسبة لـ MERGEFIELD "Column3"،
    // يمكننا تعيين اسم العمود هذا إلى MERGEFIELD في زوج المفتاح/القيمة "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // يمكننا ربط اسم عمود مصدر البيانات باسم MERGEFIELD مثل هذا.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // قم بربط عمود مصدر البيانات المسمى "Column2" بـ MERGEFIELDs المسمى "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // اسم MERGEFIELD هو "المفتاح" لاسم عمود مصدر البيانات المعني "القيمة".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // الآن إذا قمنا بتشغيل دمج البريد هذا، فستأخذ وحدات MERGEFIELD "العمود 3" البيانات من "العمود 2" بالجدول.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // يمكننا تكرار العناصر الموجودة في هذه المجموعة.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // يمكننا أيضًا إزالة العناصر من المجموعة.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// أنشئ مستندًا يحتوي على حقلي MERGEFIELD، أحدهما لا يحتوي على ملف
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
/// أنشئ جدول بيانات يتكون من عمودين، أحدهما لا يحتوي على
/// MERGEFIELD المطابق في المستند المصدر بالطريقة المذكورة أعلاه.
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

* class [MappedDataFieldCollection](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
