---
title: MailMergeCheckErrors Enum
linktitle: MailMergeCheckErrors
articleTitle: MailMergeCheckErrors
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.MailMergeCheckErrors enum على تعزيز عملية دمج البريد لديك من خلال الإبلاغ بكفاءة عن أخطاء Microsoft Word لإنشاء مستندات سلسة.
type: docs
weight: 6640
url: /ar/net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

يحدد كيفية قيام Microsoft Word بالإبلاغ عن الأخطاء التي تم اكتشافها أثناء دمج البريد.

```csharp
public enum MailMergeCheckErrors
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Simulate | `1` | محاكاة الدمج والإبلاغ عن الأخطاء في مستند جديد. |
| PauseOnError | `2` | أكمل الدمج وأوقف مؤقتًا للإبلاغ عن الأخطاء. |
| CollectErrors | `3` | أكمل عملية الدمج والإبلاغ عن الأخطاء في مستند جديد. |
| Default | `2` | يساويPauseOnError القيمة. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
