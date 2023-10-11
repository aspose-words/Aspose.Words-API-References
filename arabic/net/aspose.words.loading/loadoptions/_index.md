---
title: Class LoadOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Loading.LoadOptions فصل. يسمح بتحديد خيارات إضافية مثل كلمة المرور أو URI الأساسي عند تحميل مستند إلى ملفDocument الكائن.
type: docs
weight: 3660
url: /ar/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

يسمح بتحديد خيارات إضافية (مثل كلمة المرور أو URI الأساسي) عند تحميل مستند إلى ملف[`Document`](../../aspose.words/document/) الكائن.

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public class LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية. |
| [LoadOptions](loadoptions/#constructor_2)(string) | اختصار لتهيئة مثيل جديد لهذه الفئة بكلمة المرور المحددة لتحميل مستند مشفر. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص على القيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | الحصول على أو تعيين السلسلة التي سيتم استخدامها لتحليل معرفات URI النسبية الموجودة في المستند إلى معرفات URI مطلقة عند الحاجة. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل ملف التعريف (Wmf أوEmf ) الصور لPng تنسيق الصورة. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | الحصول على أو تعيين التشفير الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد التشفير داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | يسمح بتحديد إعدادات خط المستند. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | يحدد ما إذا كان سيتم تجاهل بيانات OLE أم لا. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | يحصل على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار معين من MS Word. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | الحصول على كلمة المرور أو تعيينها لفتح مستند مشفر. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء تحميل مستند ويقبل البيانات المتعلقة بتقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عند استيراد مستند من HTML، MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. بشكل افتراضي هذه الخاصية هي`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول ذات الامتداد أم لا`متسخ` السمة. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | يتم استدعاؤه أثناء عملية التحميل، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### أمثلة

يوضح كيفية تحميل مستند Microsoft Word المشفر.

```csharp
Document doc;

// Aspose.Words يطرح استثناءً إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// عند تحميل مثل هذا المستند، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 - قم بتحميل المستند من نظام الملفات المحلي حسب اسم الملف:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - تحميل المستند من الدفق:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)


