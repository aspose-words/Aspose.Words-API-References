---
title: Class Odso
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.Odso فصل. تحديد إعدادات كائن مصدر بيانات Office ODSO لمصدر بيانات دمج المراسلات.
type: docs
weight: 5880
url: /ar/net/aspose.words.settings/odso/
---
## Odso class

تحديد إعدادات كائن مصدر بيانات Office (ODSO) لمصدر بيانات دمج المراسلات.

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
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | يحدد الحرف الذي سيتم تفسيره على أنه محدد العمود المستخدم لفصل الأعمدة ضمن مصادر البيانات الخارجية. القيمة الافتراضية هي 0 مما يعني عدم وجود محدد عمود محدد. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | يحدد موقع مصدر البيانات الخارجي المراد توصيله بمستند لإجراء دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | تحديد نوع مصدر البيانات الخارجي المراد الاتصال به كجزء من معلومات اتصال ODSO لدمج البريد هذا. القيمة الافتراضية هيDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | الحصول على أو تعيين مجموعة من الكائنات التي تحدد كيفية تعيين الأعمدة من مصدر البيانات الخارجي إلى أسماء حقول الدمج المحددة مسبقًا في المستند. لا يتم استخدام هذا الكائن أبدًا`باطل` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | يحدد أن تطبيق الاستضافة يجب أن يتعامل مع الصف الأول من البيانات في مصدر data الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. القيمة الافتراضية هي`خطأ شنيع` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | الحصول على أو تعيين مجموعة من الكائنات التي تحدد التضمين/الاستبعاد للسجلات الفردية في دمج المراسلات. لا يتم استخدام هذا الكائن أبدًا`باطل` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | يحدد مجموعة البيانات المحددة التي يجب أن يتصل بها المصدر داخل مصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | يحدد سلسلة اتصال ارتباط البيانات العالمي (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | يُرجع نسخة عميقة من هذا الكائن. |

### ملاحظات

يبدو أن ODSO هي الطريقة "الجديدة" التي تفضل إصدارات Microsoft Word الأحدث استخدامها عند تحديد أنواع معينة من مصادر البيانات لمستند دمج البريد. ربما ظهر ODSO لأول مرة في Microsoft Word 2000.

استخدام ODSO موثق بشكل سيئ وأفضل طريقة لمعرفة كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر البيانات المطلوب يدويًا في Microsoft Word ثم فتح هذا المستند باستخدام Aspose.Words وفحص الخصائص التابع[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) و [`Odso`](../mailmergesettings/odso/)أشياء. يعد هذا أسلوبًا جيدًا إذا كنت تريد معرفة كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

لا تحتاج عادةً إلى إنشاء كائنات من هذه الفئة مباشرة لأن إعدادات ODSO متاحة دائمًا عبر[`Odso`](../mailmergesettings/odso/) ملكية.

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


