---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words OdsoDataSourceType للاتصال بسهولة بمصادر البيانات الخارجية، مما يعزز قدرات معالجة المستندات لديك.
type: docs
weight: 6720
url: /ar/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

يحدد نوع مصدر البيانات الخارجي الذي سيتم الاتصال به كجزء من معلومات اتصال ODSO.

```csharp
public enum OdsoDataSourceType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Text | `0` | يحدد أن مستندًا معينًا قد تم توصيله بملف نصي. ربما wdMergeSubTypeOther. |
| Database | `1` | يحدد أن مستندًا معينًا قد تم توصيله بقاعدة بيانات. ربما wdMergeSubTypeAccess. |
| AddressBook | `2` | يحدد أن مستندًا معينًا قد تم توصيله بدفتر عناوين جهات الاتصال. ربما wdMergeSubTypeOAL. |
| Document1 | `3` | يحدد أن مستندًا معينًا قد تم توصيله بتنسيق مستند آخر يدعمه تطبيق الإنتاج. ربما wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | يحدد أن مستندًا معينًا قد تم توصيله بتنسيق مستند آخر يدعمه تطبيق الإنتاج. ربما wdMergeSubTypeWorks. |
| Native | `5` | يحدد أن مستندًا معينًا قد تم توصيله بتنسيق مستند آخر أصلي لتطبيق الإنتاج. ربما wdMergeSubTypeOLEDBText |
| Email | `6` | يحدد أن مستندًا معينًا قد تم توصيله بتطبيق البريد الإلكتروني. ربما wdMergeSubTypeOutlook. |
| None | `7` | لم يتم تحديد نوع مصدر البيانات الخارجي. ربما wdMergeSubTypeWord. |
| Legacy | `8` | يحدد أن مستندًا معينًا قد تم توصيله بتنسيق مستند قديم يدعمه تطبيق الإنتاج ربما wdMergeSubTypeWord2000. |
| Master | `9` | يحدد أن مستندًا معينًا قد تم توصيله بمصدر بيانات يجمع مصادر بيانات أخرى. |
| Default | `7` | يساويNone . |

## ملاحظات

مواصفات OOXML لهذا التعداد مبهمة جدًا. أعتقد أنها قد تتوافق مع تعداد WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.

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

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
