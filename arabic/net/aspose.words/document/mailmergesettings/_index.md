---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words لـ .NET
description: Document MailMergeSettings ملكية. الحصول على الكائن الذي يحتوي على كافة معلومات دمج المراسلات لمستند أو تعيينه في C#.
type: docs
weight: 270
url: /ar/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

الحصول على الكائن الذي يحتوي على كافة معلومات دمج المراسلات لمستند أو تعيينه.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## ملاحظات

يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج البريد لمستند وستظهر هذه المعلومات (مع حقول البيانات المتوفرة) في Microsoft Word عندما يفتح المستخدم هذا المستند. أو يمكنك استخدام هذا الكائن للاستعلام عن إعدادات دمج البريد التي حددها المستخدم في Microsoft Word لهذا المستند.

هذا الكائن أبدا`باطل`.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
