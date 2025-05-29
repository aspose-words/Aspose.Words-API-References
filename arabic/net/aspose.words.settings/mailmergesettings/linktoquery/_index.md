---
title: MailMergeSettings.LinkToQuery
linktitle: LinkToQuery
articleTitle: LinkToQuery
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LinkToQuery في MailMergeSettings، وتعرف على كيفية التحكم في تنفيذ الاستعلام في مستندات Word وإعداداتها الافتراضية للحصول على الأداء الأمثل.
type: docs
weight: 110
url: /ar/net/aspose.words.settings/mailmergesettings/linktoquery/
---
## MailMergeSettings.LinkToQuery property

لست متأكدًا من هذا. يشير مرجع أتمتة مايكروسوفت وورد إلى أن هذا يُحدد تنفيذ الاستعلام في كل مرة يُفتح فيها المستند في مايكروسوفت وورد. لكن مواصفات OOXML تُشير إلى أن هذا يُحدد أن الاستعلام يحتوي على مرجع لملف استعلام خارجي يحتوي على الاستعلام الفعلي. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool LinkToQuery { get; set; }
```

## أمثلة

يوضح كيفية تنفيذ دمج البريد باستخدام البيانات من كائن مصدر بيانات Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// إنشاء مصدر بيانات في شكل ملف ASCII، مع حرف "|"
// يعمل كفاصل يفصل الأعمدة. يحتوي السطر الأول على أسماء الأعمدة الثلاثة.
// وكل سطر لاحق هو صف مع القيم الخاصة به.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // سيؤدي فتح هذا المستند في Microsoft Word إلى تنفيذ دمج البريد قبل عرض المحتويات.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### أنظر أيضا

* class [MailMergeSettings](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
