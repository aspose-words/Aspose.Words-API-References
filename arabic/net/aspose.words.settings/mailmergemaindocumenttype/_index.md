---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.MailMergeMainDocumentType enum، الذي يحدد أنواعًا مختلفة من مستندات المصدر لدمج البريد من أجل أتمتة المستندات بسلاسة.
type: docs
weight: 6670
url: /ar/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

يحدد الأنواع المحتملة لمستند مصدر دمج البريد.

```csharp
public enum MailMergeMainDocumentType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| NotAMergeDocument | `0` | هذه الوثيقة ليست وثيقة دمج بريدي. |
| FormLetters | `1` | يحدد أن مستند مصدر دمج البريد هو من نوع الرسالة النموذجية. |
| MailingLabels | `2` | يحدد أن مستند مصدر دمج البريد هو من نوع ملصق البريد. |
| Envelopes | `4` | يحدد أن مستند مصدر دمج البريد هو من نوع المغلف. |
| Catalog | `8` | يحدد أن مستند مصدر دمج البريد هو من نوع الكتالوج. |
| Email | `16` | يحدد أن مستند مصدر دمج البريد هو من نوع رسالة البريد الإلكتروني. |
| Fax | `32` | يحدد أن مستند مصدر دمج البريد هو من نوع الفاكس. |
| Default | `0` | يساويNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
