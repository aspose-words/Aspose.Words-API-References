---
title: Class MailMergeSettings
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.MailMergeSettings فصل. تحديد كافة معلومات دمج البريد للمستند.
type: docs
weight: 5850
url: /ar/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

تحديد كافة معلومات دمج البريد للمستند.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class MailMergeSettings
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | يحدد الفهرس الأحادي للسجل من مصدر البيانات والذي سيتم عرضه في Microsoft Word. القيمة الافتراضية هي 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. القيمة الافتراضية هي سلسلة فارغة. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | يحدد نوع الإبلاغ عن الأخطاء الذي يجب أن يتم إجراؤه بواسطة Microsoft Word عند إجراء عملية دمج البريد. القيمة الافتراضية هيDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | تحديد المسار إلى مصدر بيانات دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | تحديد نوع مصدر بيانات دمج المراسلات وطريقة الوصول إلى البيانات. القيمة الافتراضية هيDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | يحدد كيفية قيام Microsoft Word بإخراج نتائج دمج البريد. القيمة الافتراضية هيDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | يحدد كيفية تعامل التطبيق الذي يقوم بدمج المراسلات مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج المراسلات. القيمة الافتراضية هي`خطأ شنيع` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | تحديد المسار إلى مصدر رأس دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | لست متأكدًا من هذا. يشير مرجع Microsoft Word Automation إلى أن هذا يحدد تنفيذ الاستعلام في كل مرة يتم فيها فتح المستند في Microsoft Word. لكن مواصفات OOXML تشير إلى أن هذا يحدد أن الاستعلام يحتوي على مرجع لملف استعلام خارجي يحتوي على الاستعلام الفعلي. القيمة الافتراضية هي`خطأ شنيع` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | يحدد أنه يجب إرسال المستندات التي يتم إنتاجها أثناء عملية دمج البريد عبر البريد الإلكتروني كمرفق بدلاً من بدلاً من نص البريد الإلكتروني الفعلي. القيمة الافتراضية هي`خطأ شنيع` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | يحدد النص الذي يجب أن يظهر في سطر الموضوع لرسائل البريد الإلكتروني أو الفاكسات التي يتم إرسالها أثناء دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | تحديد نوع المستند الرئيسي لدمج المراسلات. القيمة الافتراضية هيDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | الحصول على الكائن الذي يحدد إعدادات كائن مصدر بيانات Office (ODSO) أو تعيينه. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | يحتوي على سلسلة لغة الاستعلام الهيكلية التي سيتم تشغيلها مقابل مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي سيتم استيرادها إلى المستند عند تنفيذ عملية دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | يحدد أن Microsoft Word يجب أن يعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (على سبيل المثال، معاينة البيانات المدمجة). القيمة الافتراضية هي`خطأ شنيع` . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | مسح إعدادات دمج البريد بحيث أنه عند حفظ المستند، لن يتم حفظ أي إعدادات لدمج البريد وسيصبح مستندًا عاديًا. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | يُرجع نسخة عميقة من هذا الكائن. |

### ملاحظات

يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج البريد لمستند وستظهر هذه المعلومات (مع حقول البيانات المتوفرة) في Microsoft Word عندما يفتح المستخدم هذا المستند. أو يمكنك استخدام هذا الكائن للاستعلام عن إعدادات دمج البريد التي حددها المستخدم في Microsoft Word لهذا المستند.

لا تحتاج عادةً إلى إنشاء كائنات من هذه الفئة مباشرة لأن إعدادات دمج البريد الخاصة بالمستند متاحة دائمًا عبر[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) ملكية.

لاكتشاف ما إذا كان هذا المستند هو مستند رئيسي لدمج المراسلات، تحقق من قيمة [`MainDocumentType`](./maindocumenttype/) ملكية.

لإزالة إعدادات دمج البريد ومعلومات مصدر البيانات من مستند، يمكنك استخدام [`Clear`](./clear/) طريقة. لن يقوم Aspose.Words بكتابة إعدادات دمج البريد في مستند إذا كان [`MainDocumentType`](./maindocumenttype/) تم تعيين الخاصية علىNotAMergeDocument أو[`DataType`](./datatype/) تم تعيين الخاصية علىNone.

أفضل طريقة لمعرفة كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات المطلوب يدويًا في Microsoft Word ثم فتح هذا المستند باستخدام Aspose.Words وفحص خصائص الخاصة بالكائن.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) و[`Odso`](./odso/) أشياء. يعد هذا أسلوبًا جيدًا يجب اتباعه إذا كنت تريد معرفة كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

يحتفظ Aspose.Words بمعلومات دمج البريد عند تحميل وحفظ وتحويل المستندات بين تنسيقات مختلفة، ولكنه لا يستخدم هذه المعلومات عند إجراء دمج البريد الخاص به باستخدام[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) هدف.

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


