---
title: "الفئة Aspose::Words::Saving::XpsSaveOptions"
linktitle: "XpsSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::Saving::XpsSaveOptions. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند بتنسيق Xps. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class


يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند بتنسيق [Xps](../../aspose.words/saveformat/). لمعرفة المزيد، زر مقالة الوثائق [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class XpsSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | يحصل على قيمة تحدد كيفية عرض الألوان. |
| [get_CompressionLevel](./get_compressionlevel/)() const | يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي [Normal](../compressionlevel/). |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | يحصل أو يعيّن المنطقة الزمنية المحلية المخصصة المستخدمة في حقول التاريخ/الوقت. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | يحصل أو يضبط كائن [DigitalSignatureDetails](../digitalsignaturedetails/) المستخدم لتوقيع مستند. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | يحصل على قيمة تحدد كيفية عرض تأثيرات 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | يحصل أو يعيّن قيمة تحدد كيفية عرض تأثيرات DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض أشكال DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | يحصل أو يضبط قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | يحصل على قيمة تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | يحصل على [NumeralFormat](../numeralformat/) المستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | العلم يشير إلى ما إذا كان من الضروري تحسين الإخراج. إذا تم تعيين هذا العلم، تُزال القنوات المتداخلة الزائدة والقنوات الفارغة، كما يتم دمج الرموز المجاورة ذات التنسيق نفسه. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية إلى **true**. القيمة الافتراضية هي **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | يسمح بتحديد خيارات المخطط. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | يحصل أو يضبط الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | عند **true**، يتم تنسيق الإخراج بشكل جميل حيثما كان ذلك ممكنًا. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | يُستدعى أثناء حفظ المستند ويقبل بيانات حول تقدم الحفظ. |
| [get_SaveFormat](./get_saveformat/)() override | يحدد التنسيق الذي سيُحفظ به المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط [Xps](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | يحدد المجلد الخاص بالملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) يتم تحديثها قبل الحفظ. القيمة الافتراضية هي **false**؛. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | يحصل على قيمة تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند إلى صيغة صفحة ثابتة. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) يتم تحديثها قبل الحفظ. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) يتم تحديثها قبل الحفظ. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | يحصل على قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر التحكم OLE. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام مضاد التسنين في العرض أم لا. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب، إذا تم تحديده عبر [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | يضبط قيمة تحدد كيفية عرض الألوان. |
| [set_CompressionLevel](./set_compressionlevel/)(Aspose::Words::Saving::CompressionLevel) | محدد لـ [Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel](./get_compressionlevel/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::DigitalSignatureDetails\>\&) | محدد لـ [Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | يضبط قيمة تحدد كيفية عرض تأثيرات الـ 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | يضبط [NumeralFormat](../numeralformat/) المستخدم في عرض الأرقام. تُستخدم الأرقام الأوروبية افتراضيًا. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | محدد لـ [Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | يضبط قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر تحكم OLE. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | محدد لـ [Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |
| [XpsSaveOptions](./xpssaveoptions/)() | ينشئ مثيلًا جديدًا لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Xps](../../aspose.words/saveformat/). |
| [XpsSaveOptions](./xpssaveoptions/)(Aspose::Words::SaveFormat) | ينشئ مثيلًا جديدًا لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Xps](../../aspose.words/saveformat/) أو [OpenXps](../../aspose.words/saveformat/). |

## أمثلة



يوضح كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند XPS المحفوظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج عناوين يمكن أن تُستخدم كمدخلات جدول المحتويات للمستويات 1 و2 ثم 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// سيتضمن مستند XPS الناتج مخططًا، جدول محتويات يسرد العناوين في جسم المستند.
// النقر على إدخال في هذا المخطط سينقلك إلى موقع العنوان المقابل.
// عيّن الخاصية "HeadingsOutlineLevels" إلى "2" لاستبعاد جميع العناوين التي مستوياتها أعلى من 2 من المخطط.
// العناوين الأخيرة التي أدرجناها أعلاه لن تظهر.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## انظر أيضًا

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
