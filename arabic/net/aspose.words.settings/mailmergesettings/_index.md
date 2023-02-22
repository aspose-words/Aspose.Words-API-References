---
title: Class MailMergeSettings
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.MailMergeSettings فصل. تحديد كافة معلومات دمج المراسلات لمستند.
type: docs
weight: 5550
url: /ar/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

تحديد كافة معلومات دمج المراسلات لمستند.

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
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | يحدد الفهرس المستند إلى واحد للسجل من مصدر البيانات والذي سيتم عرضه في Microsoft Word. القيمة الافتراضية هي 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | تحديد العمود الذي يحتوي على عناوين البريد الإلكتروني داخل مصدر البيانات. القيمة الافتراضية هي سلسلة فارغة. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | يحدد نوع الإبلاغ عن الخطأ الذي يجب أن يتم إجراؤه بواسطة Microsoft Word عند إجراء دمج المراسلات. القيمة الافتراضية هيDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | تحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | تحديد المسار إلى مصدر بيانات دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | تحديد نوع مصدر بيانات دمج المراسلات وطريقة الوصول إلى البيانات. القيمة الافتراضية هيDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | يحدد كيفية إخراج Microsoft Word لنتائج دمج المراسلات. القيمة الافتراضية هيDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | يحدد كيفية تعامل التطبيق الذي يقوم بعملية دمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. القيمة الافتراضية هي`خاطئة` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | يحدد المسار إلى مصدر رأس دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | لست متأكدًا من هذا . يشير مرجع أتمتة Microsoft Word إلى أن هذا يحدد أن الاستعلام يتم تنفيذه في كل مرة يتم فيها فتح المستند في Microsoft Word. لكن مواصفات OOXML تشير إلى أن هذا يحدد أن الاستعلام يحتوي على reference لملف استعلام خارجي يحتوي على الاستعلام الفعلي . القيمة الافتراضية هي`خاطئة` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | يحدد أن المستندات التي تم إنتاجها أثناء عملية دمج المراسلات يجب إرسالها بالبريد الإلكتروني كمرفق بدلاً من بدلاً من نص البريد الإلكتروني الفعلي. النظام الأساسي`خاطئة` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | يحدد النص الذي يجب أن يظهر في سطر الموضوع لرسائل البريد الإلكتروني أو الفاكسات التي يتم إنتاجها أثناء دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | تحديد نوع المستند الأساسي لدمج المراسلات. القيمة الافتراضية هيDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | الحصول على أو تعيين الكائن الذي يحدد إعدادات كائن مصدر بيانات Office (ODSO). |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | يحتوي على سلسلة لغة الاستعلام الهيكلية التي يجب تشغيلها مقابل مصدر البيانات الخارجي المحدد إلى لإرجاع مجموعة السجلات التي يجب استيرادها إلى المستند عند تنفيذ عملية دمج المراسلات . القيمة الافتراضية هي سلسلة فارغة . |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | يحدد أن Microsoft Word يجب أن يعرض البيانات من مصدر البيانات الخارجية المحدد حيث تم إدراج حقول الدمج (على سبيل المثال معاينة البيانات المدمجة). النظام الأساسي`خاطئة` . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | يمسح إعدادات دمج البريد بطريقة أنه عند حفظ المستند ، لن يتم حفظ أي إعدادات لدمج المراسلات وسيصبح مستندًا عاديًا. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | إرجاع نسخة عميقة من هذا الكائن. |

### ملاحظات

يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج المراسلات لمستند وستظهر هذه المعلومات (مع حقول البيانات المتاحة) في Microsoft Word عندما يفتح المستخدم هذا المستند . أو يمكنك استخدام هذا الكائن للاستعلام عن إعدادات دمج المراسلات التي حددها المستخدم في Microsoft Word لهذا المستند.

لا تحتاج عادةً إلى إنشاء كائنات من هذه الفئة مباشرةً لأن إعدادات دمج المراسلات لمستند متاحة دائمًا عبر[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) منشأه.

لاكتشاف ما إذا كان هذا المستند مستندًا أساسيًا لدمج المراسلات ، تحقق من قيمة [`MainDocumentType`](./maindocumenttype/) منشأه.

لإزالة إعدادات دمج البريد ومعلومات مصدر البيانات من مستند ، يمكنك استخدام [`Clear`](./clear/) طريقة. لن يكتب Aspose.Words إعدادات دمج البريد إلى مستند إذا كان [`MainDocumentType`](./maindocumenttype/) تم تعيين الخاصية علىNotAMergeDocument أو ملف[`DataType`](./datatype/) تم تعيين الخاصية علىNone.

أفضل طريقة لمعرفة كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات مطلوب يدويًا في Microsoft Word ثم فتح هذا المستند باستخدام Aspose.Words وفحص خصائص [`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) و[`Odso`](./odso/) أشياء. هذا طريقة جيدة لاتباعها إذا كنت تريد معرفة كيفية تكوين مصدر بيانات برمجيًا ، على سبيل المثال.

تحتفظ Aspose.Words بمعلومات دمج البريد عند تحميل وحفظ وتحويل documents بين تنسيقات مختلفة ، ولكنها لا تستخدم هذه المعلومات عند إجراء دمج المراسلات الخاص بها باستخدام[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) هدف.

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

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


