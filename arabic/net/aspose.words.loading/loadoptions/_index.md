---
title: LoadOptions
second_title: Aspose.Words لمراجع .NET API
description: يسمح بتحديد خيارات إضافية مثل كلمة المرور أو URI الأساسي عند تحميل مستند في ملفDocument../aspose.words/document الكائن .
type: docs
weight: 3460
url: /ar/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

يسمح بتحديد خيارات إضافية (مثل كلمة المرور أو URI الأساسي) عند تحميل مستند في ملف[`Document`](../../aspose.words/document) الكائن .

```csharp
public class LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LoadOptions](loadoptions#constructor)() | تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية. |
| [LoadOptions](loadoptions#constructor_2)(string) | اختصار لتهيئة مثيل جديد من هذه الفئة بكلمة المرور المحددة لتحميل مستند مشفر. |
| [LoadOptions](loadoptions#constructor_1)(LoadFormat, string, string) | اختصار لتهيئة مثيل جديد من هذه الفئة بخصائص معينة للقيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | الحصول على أو تعيين السلسلة التي سيتم استخدامها لحل URIs النسبية الموجودة في المستند إلى URIs المطلقة عند الحاجة . يمكن أن تكون سلسلة فارغة أو فارغة. الافتراضي هو فارغ. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحويل ملف تعريف (Wmf أوEmf ) صور لPng تنسيق الصورة . |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | الحصول على أو تعيين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون فارغًا. الافتراضي هو فارغ. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | يسمح بتحديد إعدادات خط الوثيقة. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | الحصول على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | الحصول على كلمة المرور أو تعيينها لفتح مستند مشفر. يمكن أن تكون سلسلة فارغة أو فارغة. الافتراضي هو فارغ. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word . القيمة الافتراضية هي false . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | يتم الاتصال به أثناء تحميل مستند ويقبل البيانات حول تقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور ، أوراق الأنماط) عند استيراد مستند من HTML ، MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. افتراضيًا ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول بامتداد`متسخ` السمة . |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | تم الاستدعاء أثناء عملية التحميل ، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |

### أمثلة

يوضح كيفية تحميل مستند Microsoft Word مشفر.

```csharp
Document doc;

// Aspose.Words استثناء إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// عند تحميل مثل هذا المستند ، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 - قم بتحميل المستند من نظام الملفات المحلي حسب اسم الملف:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - تحميل المستند من دفق:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
