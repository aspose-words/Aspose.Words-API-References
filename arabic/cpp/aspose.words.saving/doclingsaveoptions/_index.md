---
title: "Aspose::Words::Saving::DoclingSaveOptions فئة"
linktitle: "DoclingSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::DoclingSaveOptions فئة. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند بتنسيق Docling. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2750
url: /ar/cpp/aspose.words.saving/doclingsaveoptions/
---
## DoclingSaveOptions class


يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند بتنسيق [Docling](../../aspose.words/saveformat/). لمعرفة المزيد، زر مقالة الوثائق [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class DoclingSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى. |
| [DoclingSaveOptions](./doclingsaveoptions/)() |  |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | يحصل أو يعيّن المنطقة الزمنية المحلية المخصصة المستخدمة في حقول التاريخ/الوقت. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | يحصل على قيمة تحدد كيفية عرض تأثيرات 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | يحصل أو يعيّن قيمة تحدد كيفية عرض تأثيرات DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض أشكال DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | يحصل على قيمة تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | عند **true**، يتم تنسيق الإخراج بشكل جميل حيثما كان ذلك ممكنًا. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | يُستدعى أثناء حفظ المستند ويقبل بيانات حول تقدم الحفظ. |
| [get_RenderNonImageShapes](./get_rendernonimageshapes/)() const | يحصل أو يحدد قيمة تشير إلى ما إذا كان يجب عرض الأشكال غير الصورية وكتابتها إلى مستند Docling JSON الناتج. |
| [get_SaveFormat](./get_saveformat/)() override | يحدد التنسيق الذي سيُحفظ به المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط [Docling](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | يحدد المجلد الخاص بالملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) يتم تحديثها قبل الحفظ. القيمة الافتراضية هي **false**؛. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | يحصل على قيمة تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند إلى صيغة صفحة ثابتة. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) يتم تحديثها قبل الحفظ. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) يتم تحديثها قبل الحفظ. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | يحصل على قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر التحكم OLE. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام مضاد التسنين في العرض أم لا. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | يضبط قيمة تحدد كيفية عرض تأثيرات الـ 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderNonImageShapes](./set_rendernonimageshapes/)(bool) | مُعيّن لـ [Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes](./get_rendernonimageshapes/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | مُعيّن لـ [Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | يضبط قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر تحكم OLE. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية حفظ مستند بتنسيق Docling JSON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// اضبطه على true لعرض الأشكال غير الصورية وتضمينها في الناتج.
// اضبطه على false (الافتراضي) لاستبعاد الأشكال غير الصورية من الناتج.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## انظر أيضًا

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
