---
title: "فئة Aspose::Words::Loading::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Loading::TxtLoadOptions. يسمح بتحديد خيارات إضافية عند تحميل مستند نصي Text إلى كائن Document. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


يسمح بتحديد خيارات إضافية عند تحميل مستند [Text](../../aspose.words/loadformat/) إلى كائن [Document](../../aspose.words/document/). لمعرفة المزيد، زر مقالة الوثائق [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان سيتم تنفيذ اكتشاف الترقيم التلقائي أثناء تحميل مستند. القيمة الافتراضية هي **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | يحصل أو يعيّن السلسلة التي سيتم استخدامها لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل ملفات الميتا ([Wmf](../) أو [Emf](../)) إلى تنسيق الصورة [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | يحصل أو يعيّن ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office [Math](../../aspose.words.math/). |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | يحدد ما إذا كان سيتم اكتشاف الروابط التشعبية في النص. القيمة الافتراضية هي **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | يسمح بتحديد كيفية التعرف على عناصر القوائم المرقمة عندما يتم استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هي **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | يحصل أو يعيّن اتجاه المستند. القيمة الافتراضية هي [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | يحصل أو يعيّن الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون **null**. القيمة الافتراضية هي **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | يسمح بتحديد إعدادات خط المستند. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | يحصل أو يعيّن الخيار المفضل لمعالجة المسافات البادئة. القيمة الافتراضية هي [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. القيمة الافتراضية هي [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | يحصل أو يعيّن كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | يحصل أو يعيّن ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | يحدد كيفية معالجة المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | يحصل أو يضبط الخيار المفضل لمعالجة المسافات المتتبقة. القيمة الافتراضية هي [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | يحصل أو يعيّن ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | محدد لـ [Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection](./get_autonumberingdetection/). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | مُعيّن لـ [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | محدد لـ [Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks](./get_detecthyperlinks/). |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | محدد لـ [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | محدد لـ [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | محدد لـ [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | يُستدعى أثناء تحميل المستند ويقبل بيانات حول تقدم التحميل. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | محدد لـ [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | المحدد لـ [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [TxtLoadOptions](./txtloadoptions/)() | ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية قراءة وعرض الروابط التشعبية.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // تحميل المستند مع الروابط التشعبية.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // طباعة نص الروابط التشعبية.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## انظر أيضًا

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
