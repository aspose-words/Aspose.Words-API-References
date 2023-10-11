---
title: Enum OdsoDataSourceType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.OdsoDataSourceType تعداد. يحدد نوع مصدر البيانات الخارجي المراد الاتصال به كجزء من معلومات اتصال ODSO.
type: docs
weight: 5890
url: /ar/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

يحدد نوع مصدر البيانات الخارجي المراد الاتصال به كجزء من معلومات اتصال ODSO.

```csharp
public enum OdsoDataSourceType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Text | `0` | يحدد أنه تم ربط مستند معين بملف نصي. ربما wdMergeSubTypeOther. |
| Database | `1` | يحدد أن مستندًا معينًا قد تم توصيله بقاعدة بيانات. ربما wdMergeSubTypeAccess. |
| AddressBook | `2` | يحدد أن مستندًا معينًا قد تم توصيله بسجل عناوين جهات الاتصال. من المحتمل wdMergeSubTypeOAL. |
| Document1 | `3` | يحدد أنه تم توصيل مستند معين بتنسيق مستند آخر يدعمه التطبيق المنتج. من المحتمل wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | يحدد أنه تم ربط مستند معين بتنسيق مستند آخر يدعمه التطبيق المنتج. من المحتمل wdMergeSubTypeWorks. |
| Native | `5` | يحدد أنه تم توصيل مستند معين بتنسيق مستند آخر أصلي للتطبيق المنتج. من المحتمل wdMergeSubTypeOLEDBText |
| Email | `6` | يحدد أن مستندًا معينًا قد تم توصيله بتطبيق بريد إلكتروني. من المحتمل wdMergeSubTypeOutlook. |
| None | `7` | لم يتم تحديد نوع مصدر البيانات الخارجي. من المحتمل wdMergeSubTypeWord. |
| Legacy | `8` | يحدد أن مستندًا معينًا قد تم توصيله بتنسيق مستند قديم يدعمه التطبيق المنتج من المحتمل wdMergeSubTypeWord2000. |
| Master | `9` | يحدد أنه تم ربط مستند معين بمصدر بيانات يقوم بتجميع مصادر البيانات الأخرى. |
| Default | `7` | يساويNone . |

### ملاحظات

مواصفات OOXML غامضة جدًا لهذا التعداد. أعتقد أنه قد يتوافق مع تعداد WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.

### أمثلة

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

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


