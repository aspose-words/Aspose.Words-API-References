---
title: Enum MailMergeMainDocumentType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.MailMergeMainDocumentType تعداد. تحديد الأنواع المحتملة للمستند المصدر لدمج المراسلات.
type: docs
weight: 5840
url: /ar/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

تحديد الأنواع المحتملة للمستند المصدر لدمج المراسلات.

```csharp
public enum MailMergeMainDocumentType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| NotAMergeDocument | `0` | هذا المستند ليس مستند دمج بريد. |
| FormLetters | `1` | تحديد أن المستند المصدر لدمج المراسلات هو من نوع الرسالة النموذجية. |
| MailingLabels | `2` | تحديد أن المستند المصدر لدمج المراسلات هو من نوع التسمية البريدية. |
| Envelopes | `4` | تحديد أن المستند المصدر لدمج المراسلات من نوع المغلف. |
| Catalog | `8` | تحديد أن المستند المصدر لدمج المراسلات من نوع الكتالوج. |
| Email | `16` | تحديد أن المستند المصدر لدمج المراسلات هو من نوع رسالة البريد الإلكتروني. |
| Fax | `32` | تحديد أن المستند المصدر لدمج المراسلات من نوع الفاكس. |
| Default | `0` | يساويNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


