---
title: Enum MailMergeDestination
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.MailMergeDestination تعداد. يحدد النتائج المحتملة التي قد يتم إنشاؤها عند تنفيذ عملية دمج البريد على مستند.
type: docs
weight: 5830
url: /ar/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

يحدد النتائج المحتملة التي قد يتم إنشاؤها عند تنفيذ عملية دمج البريد على مستند.

```csharp
public enum MailMergeDestination
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| NewDocument | `0` | يحدد أن تطبيقات الاستضافة المطابقة يجب أن تنشئ مستندات جديدة عن طريق ملء الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد. |
| Printer | `1` | يحدد أن تطبيقات الاستضافة المطابقة يجب أن تطبع المستندات الناتجة عن ملء حقول داخل مستند معين ببيانات خارجية من مصدر البيانات الخارجي المحدد. |
| Email | `2` | يحدد أن تطبيقات الاستضافة المطابقة يجب أن تنشئ رسائل بريد إلكتروني باستخدام المستندات الناتجة عن ملء الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد. |
| Fax | `4` | يحدد أن تطبيقات الاستضافة المطابقة يجب أن تقوم بإنشاء فاكسات باستخدام المستندات الناتجة عن ملء الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد. |
| Default | `0` | يساويNewDocument القيمة. |

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

* property [Destination](../mailmergesettings/destination/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


