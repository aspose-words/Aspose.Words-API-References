---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.MailMergeSettings لتبسيط أتمتة المستندات باستخدام إمكانيات دمج البريد القوية لتحسين الكفاءة.
type: docs
weight: 6680
url: /ar/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

يحدد كافة معلومات دمج البريد لمستند.

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
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | يُحدد فهرس السجل من مصدر البيانات الذي سيتم عرضه في Microsoft Word. القيمة الافتراضية هي 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | يحدد العمود الذي يحتوي على عناوين البريد الإلكتروني في مصدر البيانات. القيمة الافتراضية هي سلسلة فارغة. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | يحدد نوع تقرير الخطأ الذي يجب أن يقوم به Microsoft Word عند تنفيذ دمج البريد. القيمة الافتراضية هيDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية سلسلة فارغة. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | يحدد مسار مصدر بيانات دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | يحدد نوع مصدر بيانات الدمج البريدي وطريقة الوصول إلى البيانات. القيمة الافتراضية هيDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | يحدد كيفية قيام Microsoft Word بإخراج نتائج دمج البريد. القيمة الافتراضية هيDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | يحدد كيفية تعامل التطبيق الذي يقوم بدمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. القيمة الافتراضية هي`خطأ شنيع` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | يحدد المسار إلى مصدر رأس الدمج البريدي. القيمة الافتراضية هي سلسلة فارغة. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | لست متأكدًا من هذا. يشير مرجع أتمتة مايكروسوفت وورد إلى أن هذا يُحدد تنفيذ الاستعلام في كل مرة يُفتح فيها المستند في مايكروسوفت وورد. لكن مواصفات OOXML تُشير إلى أن هذا يُحدد أن الاستعلام يحتوي على مرجع لملف استعلام خارجي يحتوي على الاستعلام الفعلي. القيمة الافتراضية هي`خطأ شنيع` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | يُحدد أنه يجب إرسال المستندات الناتجة أثناء عملية دمج البريد كمرفقات بدلاً من كنص للبريد الإلكتروني نفسه. القيمة الافتراضية هي`خطأ شنيع` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | يحدد النص الذي يجب أن يظهر في سطر الموضوع في رسائل البريد الإلكتروني أو الفاكسات التي يتم إنتاجها أثناء دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | يحدد نوع المستند الرئيسي للدمج البريدي. القيمة الافتراضية هيDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | يحصل على الكائن الذي يحدد إعدادات كائن مصدر بيانات Office (ODSO) أو يعينه. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | يحتوي على سلسلة لغة الاستعلام المنظمة التي يجب تشغيلها على مصدر البيانات الخارجي المحدد لـ إرجاع مجموعة السجلات التي يجب استيرادها إلى المستند عند تنفيذ عملية دمج البريد. القيمة الافتراضية هي سلسلة فارغة. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | يُحدد أن مايكروسوفت وورد سيعرض البيانات من مصدر البيانات الخارجي المُحدد الذي أُدرجت فيه حقول الدمج (مثل معاينة البيانات المدمجة). القيمة الافتراضية هي`خطأ شنيع` . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | يقوم بمسح إعدادات دمج البريد بطريقة تجعل لا يتم حفظ أي إعدادات لدمج البريد عند حفظ المستند، وسيصبح مستندًا عاديًا. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | يعيد نسخة طبق الأصل من هذا الكائن. |

## ملاحظات

يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج البريد لمستند، وستظهر هذه المعلومات (إلى جانب حقول البيانات المتوفرة) في Microsoft Word عندما يفتح المستخدم هذا المستند. أو يمكنك استخدام هذا الكائن للاستعلام عن إعدادات دمج البريد التي حددها المستخدم في Microsoft Word لهذا المستند.

لا تحتاج عادةً إلى إنشاء كائنات من هذه الفئة مباشرةً لأن إعدادات دمج البريد للمستند متاحة دائمًا عبر[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) ملكية.

لكشف ما إذا كان هذا المستند مستندًا رئيسيًا لدمج البريد، تحقق من قيمة [`MainDocumentType`](./maindocumenttype/) ملكية.

لإزالة إعدادات دمج البريد ومعلومات مصدر البيانات من مستند، يمكنك استخدام [`Clear`](./clear/) الطريقة. لن يكتب Aspose.Words إعدادات دمج البريد إلى مستند إذا كان [`MainDocumentType`](./maindocumenttype/) تم تعيين الخاصية إلىNotAMergeDocument أو[`DataType`](./datatype/) تم تعيين الخاصية إلىNone.

أفضل طريقة لتعلم كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات المطلوب يدويًا في Microsoft Word ثم فتح هذا المستند باستخدام Aspose.Words وفحص خصائص [`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) و[`Odso`](./odso/) الكائنات. هذا هو نهج جيد يمكنك اتباعه إذا كنت تريد أن تتعلم كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

يحتفظ Aspose.Words بمعلومات دمج البريد عند تحميل المستندات وحفظها وتحويلها بين تنسيقات مختلفة، ولكنه لا يستخدم هذه المعلومات عند تنفيذ دمج البريد الخاص به باستخدام[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) هدف.

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
