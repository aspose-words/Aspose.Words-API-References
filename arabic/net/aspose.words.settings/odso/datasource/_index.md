---
title: Odso.DataSource
linktitle: DataSource
articleTitle: DataSource
second_title: Aspose.Words لـ .NET
description: Odso DataSource ملكية. يحدد موقع مصدر البيانات الخارجي المراد توصيله بمستند لإجراء دمج البريد. القيمة الافتراضية هي سلسلة فارغة في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/odso/datasource/
---
## Odso.DataSource property

يحدد موقع مصدر البيانات الخارجي المراد توصيله بمستند لإجراء دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string DataSource { get; set; }
```

## أمثلة

يوضح كيفية تنفيذ دمج البريد مع البيانات من كائن مصدر بيانات Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// قم بإنشاء مصدر بيانات على شكل ملف ASCII، باستخدام "|" شخصية
// يعمل كمحدد يفصل بين الأعمدة. السطر الأول يحتوي على أسماء الأعمدة الثلاثة،
// وكل سطر لاحق عبارة عن صف بقيمه الخاصة.
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

* class [Odso](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
