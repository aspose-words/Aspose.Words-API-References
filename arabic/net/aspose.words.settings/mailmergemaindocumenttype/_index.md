---
title: Enum MailMergeMainDocumentType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.MailMergeMainDocumentType تعداد. تحديد الأنواع الممكنة لمستند مصدر دمج المراسلات.
type: docs
weight: 5540
url: /ar/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

تحديد الأنواع الممكنة لمستند مصدر دمج المراسلات.

```csharp
public enum MailMergeMainDocumentType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| NotAMergeDocument | `0` | هذا المستند ليس مستند دمج مراسلات . |
| FormLetters | `1` | تحديد أن المستند المصدر لدمج المراسلات من نوع الحرف النموذجي. |
| MailingLabels | `2` | تحديد أن مستند مصدر دمج المراسلات من نوع التسمية البريدية. |
| Envelopes | `4` | تحديد أن المستند المصدر لدمج المراسلات من نوع المغلف. |
| Catalog | `8` | تحديد أن المستند المصدر لدمج المراسلات من نوع الكتالوج. |
| Email | `16` | تحديد أن المستند المصدر لدمج المراسلات من نوع رسالة البريد الإلكتروني. |
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

// إنشاء مصدر بيانات في شكل ملف ASCII ، باستخدام "|" حرف
// يعمل كمحدد يفصل بين الأعمدة. يحتوي السطر الأول على أسماء الأعمدة الثلاثة ،
// وكل سطر لاحق هو صف بقيمها الخاصة.
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


