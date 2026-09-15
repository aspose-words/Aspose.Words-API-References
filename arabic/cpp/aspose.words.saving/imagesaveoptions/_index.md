---
title: "Aspose::Words::Saving::ImageSaveOptions class"
linktitle: "ImageSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions class. يسمح بتحديد خيارات إضافية عند عرض صفحات المستند أو الأشكال إلى صور. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class


يسمح بتحديد خيارات إضافية عند تحويل صفحات المستند أو الأشكال إلى صور. لمعرفة المزيد، زر مقالة الوثائق [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class ImageSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | ينشئ نسخة عميقة من هذا الكائن. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | يحصل على قيمة تحدد كيفية عرض الألوان. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | يحصل أو يعيّن المنطقة الزمنية المحلية المخصصة المستخدمة في حقول التاريخ/الوقت. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | يحصل على قيمة تحدد كيفية عرض تأثيرات 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | يحصل أو يعيّن قيمة تحدد كيفية عرض تأثيرات DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض أشكال DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**. |
| [get_GraphicsQualityOptions](./get_graphicsqualityoptions/)() const | يسمح بتحديد وضع العرض والجودة لكائن **Graphics**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | يحصل أو يضبط الدقة الأفقية للصور المُولَّدة، بالنقاط في البوصة. |
| [get_ImageBrightness](./get_imagebrightness/)() const | يحصل أو يضبط السطوع للصور المُولَّدة. |
| [get_ImageColorMode](./get_imagecolormode/)() const | يحصل أو يضبط وضع اللون للصور المُولَّدة. |
| [get_ImageContrast](./get_imagecontrast/)() const | يحصل أو يضبط التباين للصور المُولَّدة. |
| [get_ImageSize](./get_imagesize/)() const | يحصل أو يضبط حجم الصورة المُولَّدة بالبكسل. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [get_JpegQuality](./get_jpegquality/)() | يحصل أو يضبط قيمة تحدد جودة صور JPEG المُولَّدة. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | يحصل أو يضبط قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | يحصل على قيمة تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_MetafileRenderingOptions](./get_metafilerenderingoptions/)() | يسمح بتحديد كيفية معالجة ملفات التعريف في الناتج المعروض. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | يحصل على [NumeralFormat](../numeralformat/) المستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | العلم يشير إلى ما إذا كان من الضروري تحسين الإخراج. إذا تم تعيين هذا العلم، تُزال القنوات المتداخلة الزائدة والقنوات الفارغة، كما يتم دمج الرموز المجاورة ذات التنسيق نفسه. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية إلى **true**. القيمة الافتراضية هي **false**. |
| [get_PageLayout](./get_pagelayout/)() const | يحصل أو يضبط التخطيط المستخدم عند عرض صفحات متعددة في مخرج واحد. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [get_PageSet](./get_pageset/)() | يحصل أو يضبط الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | يحصل أو يضبط الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند. |
| [get_PaperColor](./get_papercolor/)() | يحصل أو يضبط لون الخلفية (الورق) للصور المُولَّدة. القيمة الافتراضية هي **White**. |
| [get_PixelFormat](./get_pixelformat/)() const | يحصل أو يضبط تنسيق البكسل للصور المُولَّدة. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | عند **true**، يتم تنسيق الإخراج بشكل جميل حيثما كان ذلك ممكنًا. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | يُستدعى أثناء حفظ المستند ويقبل بيانات حول تقدم الحفظ. |
| [get_SaveFormat](./get_saveformat/)() override | يحدد التنسيق الذي سيتم حفظ صفحات المستند أو الأشكال المعروضة به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون تنسيق نقطي [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/) أو تنسيق متجه [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../), [Svg](../../aspose.words/saveformat/). |
| [get_Scale](./get_scale/)() const | يحصل أو يضبط عامل التكبير للصور المُولَّدة. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | يحدد المجلد الخاص بالملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/)() const | يحصل أو يضبط العتبة التي تحدد قيمة خطأ التثنائي في طريقة فلويد-ستينبرغ. عندما يكون [ImageBinarizationMethod](../imagebinarizationmethod/) هو [FloydSteinbergDithering](../imagebinarizationmethod/). |
| [get_TiffBinarizationMethod](./get_tiffbinarizationmethod/)() const | يحصل أو يضبط الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 bpp عندما يكون [SaveFormat](./get_saveformat/) هو [Tiff](../../aspose.words/saveformat/) و [TiffCompression](./get_tiffcompression/) يساوي [Ccitt3](../tiffcompression/) أو [Ccitt4](../tiffcompression/). |
| [get_TiffCompression](./get_tiffcompression/)() const | يحصل أو يضبط نوع الضغط لتطبيقه عند حفظ الصور المُولَّدة بتنسيق TIFF. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) يتم تحديثها قبل الحفظ. القيمة الافتراضية هي **false**؛. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | يحصل على قيمة تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند إلى صيغة صفحة ثابتة. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) يتم تحديثها قبل الحفظ. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) يتم تحديثها قبل الحفظ. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | يحصل على قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر التحكم OLE. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام مضاد التسنين في العرض أم لا. |
| [get_UseGdiEmfRenderer](./get_usegdiemfrenderer/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام GDI+ أو مُعالج ملفات الميتا Aspose.Words عند الحفظ إلى EMF. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [get_VerticalResolution](./get_verticalresolution/)() const | يحصل أو يضبط الدقة العمودية للصور المُولَّدة، بوحدة النقاط في البوصة. |
| [GetType](./gettype/)() const override |  |
| [ImageSaveOptions](./imagesaveoptions/)(Aspose::Words::SaveFormat) | يُنشئ مثيلاً جديداً من هذه الفئة يمكن استخدامه لحفظ الصور المُصدَّرة بتنسيق [Tiff](../../aspose.words/saveformat/)، [Png](../../aspose.words/saveformat/)، [Bmp](../../aspose.words/saveformat/)، [Jpeg](../../aspose.words/saveformat/)، [Emf](../../aspose.words/saveformat/)، [Eps](../../aspose.words/saveformat/)، [WebP](../) أو بتنسيق [Svg](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | يضبط قيمة تحدد كيفية عرض الألوان. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | يضبط قيمة تحدد كيفية عرض تأثيرات الـ 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_GraphicsQualityOptions](./set_graphicsqualityoptions/)(const System::SharedPtr\<Aspose::Words::Saving::GraphicsQualityOptions\>\&) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_GraphicsQualityOptions](./get_graphicsqualityoptions/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(float) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_ImageBrightness](./set_imagebrightness/)(float) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness](./get_imagebrightness/). |
| [set_ImageColorMode](./set_imagecolormode/)(Aspose::Words::Saving::ImageColorMode) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode](./get_imagecolormode/). |
| [set_ImageContrast](./set_imagecontrast/)(float) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast](./get_imagecontrast/). |
| [set_ImageSize](./set_imagesize/)(System::Drawing::Size) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_ImageSize](./get_imagesize/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | يضبط [NumeralFormat](../numeralformat/) المستخدم في عرض الأرقام. تُستخدم الأرقام الأوروبية افتراضيًا. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(const System::SharedPtr\<Aspose::Words::Saving::MultiPageLayout\>\&) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_PageLayout](./get_pagelayout/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [set_PageSet](./set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_PageSet](./get_pageset/). |
| [set_PaperColor](./set_papercolor/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_PaperColor](./get_papercolor/). |
| [set_PixelFormat](./set_pixelformat/)(Aspose::Words::Saving::ImagePixelFormat) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat](./get_pixelformat/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_Resolution](./set_resolution/)(float) | يضبط كلًا من الدقة الأفقية والعمودية للصور المُولَّدة، بوحدة النقاط في البوصة. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_Scale](./set_scale/)(float) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_Scale](./get_scale/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_ThresholdForFloydSteinbergDithering](./set_thresholdforfloydsteinbergdithering/)(uint8_t) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/). |
| [set_TiffBinarizationMethod](./set_tiffbinarizationmethod/)(Aspose::Words::Saving::ImageBinarizationMethod) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod](./get_tiffbinarizationmethod/). |
| [set_TiffCompression](./set_tiffcompression/)(Aspose::Words::Saving::TiffCompression) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression](./get_tiffcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | يضبط قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر تحكم OLE. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseGdiEmfRenderer](./set_usegdiemfrenderer/)(bool) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer](./get_usegdiemfrenderer/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_VerticalResolution](./set_verticalresolution/)(float) | مُعيّن لـ [Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution](./get_verticalresolution/). |
| static [Type](./type/)() |  |

## أمثلة



يُصوّر صفحة من مستند Word إلى صورة بخلفية شفافة أو ملونة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// اضبط الخاصية "PaperColor" إلى لون شفاف لتطبيق شفاف
// خلفية للمستند أثناء تحويله إلى صورة.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// اضبط الخاصية "PaperColor" إلى لون غير شفاف لتطبيق ذلك اللون
// كخلفية للمستند أثناء تحويله إلى صورة.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```


يوضح كيفية تكوين الضغط أثناء حفظ المستند كملف JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// اضبط الخاصية "JpegQuality" إلى "10" لاستخدام ضغط أقوى عند تحويل المستند.
// سيؤدي ذلك إلى تقليل حجم ملف المستند، لكن الصورة ستظهر آثار ضغط أكثر وضوحًا.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// اضبط الخاصية "JpegQuality" إلى "100" لاستخدام ضغط أضعف عند rending المستند.
// سيحسن ذلك جودة الصورة على حساب زيادة حجم الملف.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```


يوضح كيفية تحديد الدقة أثناء تحويل المستند إلى PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// اضبط الخاصية "Resolution" إلى "72" لتحويل المستند بدقة 72dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// اضبط الخاصية "Resolution" إلى "300" لتحويل المستند بدقة 300dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## انظر أيضًا

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
