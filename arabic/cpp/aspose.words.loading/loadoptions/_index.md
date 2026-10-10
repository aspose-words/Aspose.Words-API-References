---
title: "فئة Aspose::Words::Loading::LoadOptions"
linktitle: "LoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Loading::LoadOptions. تسمح بتحديد خيارات إضافية (مثل كلمة المرور أو عنوان URI الأساسي) عند تحميل مستند إلى كائن Document. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


تسمح بتحديد خيارات إضافية (مثل كلمة المرور أو عنوان URI الأساسي) عند تحميل مستند إلى كائن [Document](../../aspose.words/document/). لمعرفة المزيد، زر مقالة الوثائق [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LoadOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_BaseUri](./get_baseuri/)() const | يحصل أو يعيّن السلسلة التي سيتم استخدامها لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل ملفات الميتا ([Wmf](../) أو [Emf](../)) إلى تنسيق الصورة [Png](../). |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office [Math](../../aspose.words.math/). |
| [get_Encoding](./get_encoding/)() const | يحصل أو يعيّن الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون **null**. القيمة الافتراضية هي **null**. |
| [get_FontSettings](./get_fontsettings/)() const | يسمح بتحديد إعدادات خط المستند. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند. |
| [get_LoadFormat](./get_loadformat/)() const | يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. القيمة الافتراضية هي [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | يحصل أو يعيّن كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | يحصل أو يعيّن ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [get_RecoveryMode](./get_recoverymode/)() const | يحدد كيفية معالجة المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [get_TempFolder](./get_tempfolder/)() const | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة **dirty**. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | يحصل أو يعيّن ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [get_WarningCallback](./get_warningcallback/)() const | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [LoadOptions](./loadoptions/)(const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/). |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/). |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/). |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/). |
| [set_Password](./set_password/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/). |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | دالة ضبط لـ [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/). |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية تحميل مستند Microsoft Word مشفر.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// تقوم Aspose.Words بإلقاء استثناء إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// عند تحميل مثل هذا المستند، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 -  تحميل المستند من نظام الملفات المحلي باستخدام اسم الملف:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  تحميل المستند من تدفق:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
