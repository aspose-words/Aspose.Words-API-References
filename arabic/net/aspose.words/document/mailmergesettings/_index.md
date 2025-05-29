---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية MailMergeSettings لإدارة جميع بيانات دمج البريد الخاصة بمستندك بكفاءة وتحسين سير عملك.
type: docs
weight: 280
url: /ar/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

يحصل على الكائن الذي يحتوي على كافة معلومات دمج البريد لمستند أو يعينه.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## ملاحظات

يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج البريد لمستند، وستظهر هذه المعلومات (إلى جانب حقول البيانات المتوفرة) في Microsoft Word عندما يفتح المستخدم هذا المستند. أو يمكنك استخدام هذا الكائن للاستعلام عن إعدادات دمج البريد التي حددها المستخدم في Microsoft Word لهذا المستند.

هذا الكائن لا يحدث أبدًا`باطل`.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
