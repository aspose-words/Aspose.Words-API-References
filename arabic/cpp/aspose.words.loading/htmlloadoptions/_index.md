---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::HtmlLoadOptions class. يسمح بتحديد خيارات إضافية عند تحميل مستند HTML إلى كائن Document. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


يسمح بتحديد خيارات إضافية عند تحميل مستند HTML إلى كائن [Document](../../aspose.words/document/). لمعرفة المزيد، قم بزيارة مقالة الوثائق [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | يحصل أو يعيّن السلسلة التي سيتم استخدامها لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_BlockImportMode](./get_blockimportmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية استيراد خصائص العناصر على مستوى الكتلة. القيمة الافتراضية هي [Merge](../blockimportmode/). |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل ملفات الميتا ([Wmf](../) أو [Emf](../)) إلى تنسيق الصورة [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office [Math](../../aspose.words.math/). |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | يحصل أو يعيّن قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. القيمة الافتراضية هي **false**، وإذا كان ذلك ممكنًا، تُحفظ صور SVG المحملة كما هي دون تحويل. |
| [get_Encoding](../loadoptions/get_encoding/)() const | يحصل أو يعيّن الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون **null**. القيمة الافتراضية هي **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | يسمح بتحديد إعدادات خط المستند. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | يحصل أو يعيّن قيمة تشير إلى ما إذا كان يجب تجاهل عناصر HTML <noscript>. القيمة الافتراضية هي **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. القيمة الافتراضية هي [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | يحصل أو يعيّن كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | يحصل أو يعيّن النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة <input> و <select>. القيمة الافتراضية هي [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | يحصل أو يعيّن ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | يحدد كيفية معالجة المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | يحصل أو يعيّن قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة. القيمة الافتراضية هي **false**. |
| [get_SupportVml](./get_supportvml/)() const | يحصل أو يعيّن قيمة تشير إلى ما إذا كان يجب دعم صور VML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | يحصل أو يعيّن ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | عدد المللي ثانية للانتظار قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | مُعيّن لـ [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | مُعيّن لـ [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | المحدد لـ [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | المحدد لـ [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | المحدد لـ [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | المحدد لـ [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | المحدد لـ [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | عدد المللي ثانية للانتظار قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية). |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// إذا كانت القيمة true، فإننا نأخذ شفرة VML في الاعتبار أثناء تحليل المستند المحمَّل.
loadOptions->set_SupportVml(supportVml);

// يحتوي هذا المستند على صورة JPEG داخل وسوم "<!--[if gte vml 1]>"،
// و صورة PNG مختلفة داخل وسوم "<![if !vml]>".
// إذا قمنا بتعيين العلامة "SupportVml" إلى "true"، فستقوم Aspose.Words بتحميل صورة JPEG.
// إذا قمنا بتعيين هذه العلامة إلى "false"، فستقوم Aspose.Words بتحميل صورة PNG فقط.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## انظر أيضًا

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
