---
title: "Aspose::Words::Loading::ChmLoadOptions class"
linktitle: "ChmLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::ChmLoadOptions class. يسمح بتحديد خيارات إضافية عند تحميل مستند CHM إلى كائن Document. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class


يسمح بتحديد خيارات إضافية عند تحميل مستند CHM إلى كائن [Document](../../aspose.words/document/). لمعرفة المزيد، زر مقالة الوثائق [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ChmLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ChmLoadOptions](./chmloadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | يحصل أو يعيّن السلسلة التي سيتم استخدامها لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل ملفات الميتا ([Wmf](../) أو [Emf](../)) إلى تنسيق الصورة [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office [Math](../../aspose.words.math/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | يحصل أو يعيّن الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون **null**. القيمة الافتراضية هي **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | يسمح بتحديد إعدادات خط المستند. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. القيمة الافتراضية هي [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_OriginalFileName](./get_originalfilename/)() const | اسم ملف CHM. القيمة الافتراضية هي **null**. |
| [get_Password](../loadoptions/get_password/)() const | يحصل أو يعيّن كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | يحصل أو يعيّن ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | يحدد كيفية معالجة المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | يحصل أو يعيّن ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | مُعيّن لـ [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_OriginalFileName](./set_originalfilename/)(const System::String\&) | دالة تعيين لـ [Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName](./get_originalfilename/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية حل عناوين URL مثل "ms-its:myfile.chm::/index.htm".
```cpp
// يحتوي مستندنا على عناوين URL مثل "ms-its:amhelp.chm::....htm"، لكنه يحمل اسمًا مختلفًا،
// لذلك لا تعمل روابط الملفات بعد حفظه كـ HTML.
// نحتاج إلى تحديد اسم الملف الأصلي في 'ChmLoadOptions' لتجنب هذا السلوك.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## انظر أيضًا

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
