---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Settings.Odso لدمج سلس لدمج البريد. حسّن إعدادات ODSO لإدارة مصادر البيانات بكفاءة.
type: docs
weight: 6710
url: /ar/net/aspose.words.settings/odso/
---
## Odso class

يحدد إعدادات كائن مصدر بيانات Office (ODSO) لمصدر بيانات دمج البريد.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class Odso
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Odso](odso/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | يحدد الحرف الذي يجب تفسيره على أنه فاصل العمود المستخدم لفصل الأعمدة داخل مصادر البيانات الخارجية. القيمة الافتراضية هي 0 مما يعني أنه لا يوجد فاصل عمود محدد. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | يحدد موقع مصدر البيانات الخارجي الذي سيتم توصيله بالمستند لأداء دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | يحدد نوع مصدر البيانات الخارجي الذي سيتم الاتصال به كجزء من معلومات اتصال ODSO لدمج البريد هذا. القيمة الافتراضية هيDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | يحصل على مجموعة من الكائنات أو يعينها، والتي تحدد كيفية تعيين الأعمدة من مصدر البيانات الخارجي إلى أسماء حقول الدمج المحددة مسبقًا في المستند. لا يتم حفظ هذا الكائن أبدًا`باطل` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | يحدد أن تطبيق الاستضافة يجب أن يعامل الصف الأول من البيانات في مصدر البيانات الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. القيمة الافتراضية هي`خطأ شنيع` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | يحصل على مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد أو يعينها. لا يتم تضمين هذا الكائن أبدًا`باطل` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | يحدد مجموعة البيانات المحددة التي يجب أن يتصل بها المصدر داخل مصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | يحدد سلسلة اتصال ارتباط البيانات العالمي (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | يعيد نسخة طبق الأصل من هذا الكائن. |

## ملاحظات

يبدو أن ODSO هي الطريقة "الجديدة" التي تُفضّل إصدارات Microsoft Word الأحدث استخدامها لتحديد أنواع معينة من مصادر البيانات لمستند دمج البريد. يُرجّح أن ODSO ظهر لأول مرة في Microsoft Word 2000.

إن استخدام ODSO موثق بشكل سيئ وأفضل طريقة لتعلم كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر البيانات المطلوب يدويًا في Microsoft Word ثم فتح هذا المستند باستخدام Aspose.Words وفحص خصائص[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) و [`Odso`](../mailmergesettings/odso/)الكائنات. يُعد هذا نهجًا جيدًا يمكنك اتباعه إذا كنت تريد معرفة كيفية تكوين مصدر بيانات برمجيًا باستخدام ، على سبيل المثال.

لا تحتاج عادةً إلى إنشاء كائنات من هذه الفئة مباشرةً لأن إعدادات ODSO متوفرة دائمًا عبر[`Odso`](../mailmergesettings/odso/) ملكية.

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
