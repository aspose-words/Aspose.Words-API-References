---
title: "فئة Aspose::Words::Saving::HtmlFixedSaveOptions"
linktitle: "HtmlFixedSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::HtmlFixedSaveOptions. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند إلى تنسيق HtmlFixed. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند إلى تنسيق [HtmlFixed](../../aspose.words/saveformat/) . لمعرفة المزيد، زر مقالة الوثائق [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | يحصل على قيمة تحدد كيفية عرض الألوان. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | يحدد البادئة التي تُضاف إلى جميع أسماء الفئات في ملف style.css. القيمة الافتراضية هي **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | يحصل أو يعيّن المنطقة الزمنية المحلية المخصصة المستخدمة في حقول التاريخ/الوقت. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | يحصل على قيمة تحدد كيفية عرض تأثيرات 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | يحصل أو يعيّن قيمة تحدد كيفية عرض تأثيرات DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض أشكال DrawingML. |
| [get_Encoding](./get_encoding/)() const | يحدد الترميز المستخدم عند التصدير إلى HTML. القيمة الافتراضية هي **new UTF8Encoding(true)** (UTF-8 مع BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | يحدد ما إذا كان يجب تضمين CSS (Cascading [Style](../../aspose.words/style/) Sheet) في مستند Html. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | يحدد ما إذا كان يجب تضمين الخطوط في مستند Html بتنسيق Base64. ملاحظة: ضبط هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف Html الناتج. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | يحدد ما إذا كان يجب تضمين الصور في مستند Html بتنسيق Base64. ملاحظة: ضبط هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف Html الناتج. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | يحدد ما إذا كان يجب تضمين موارد SVG في مستند Html. القيمة الافتراضية هي **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | يحصل أو يضبط إشارة ما إذا كانت حقول النموذج تُصدّر كعناصر تفاعلية (كوسم 'input') بدلاً من تحويلها إلى نص أو رسومات. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**. |
| [get_FontFormat](./get_fontformat/)() const | يحصل أو يضبط [ExportFontFormat](../exportfontformat/) المستخدم لتصدير الخطوط. القيمة الافتراضية هي [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | يحدد بادئة تُضاف إلى جميع معرّفات العناصر المُنشأة في المستند الناتج. القيمة الافتراضية هي null ولا تُضاف أي بادئة. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | يحصل أو يضبط قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | يحصل على قيمة تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | يحصل على [NumeralFormat](../numeralformat/) المستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | العلم يشير إلى ما إذا كان من الضروري تحسين المخرجات. إذا تم ضبط هذا العلم، تُزال القواميس المتداخلة الزائدة والكانفاس الفارغ، كما تُدمج الحروف المجاورة ذات التنسيق نفسه. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم ضبط هذه الخاصية إلى **true**. القيمة الافتراضية هي **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | يحدد محاذاة الصفحات أفقياً في مستند HTML. القيمة الافتراضية هي [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | يحدد الهوامش حول الصفحات في مستند HTML. تُقاس قيمة الهوامش بالنقاط ويجب أن تكون مساوية أو أكبر من 0. القيمة الافتراضية هي 10 نقاط. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | يحصل أو يضبط الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | عند **true**، يتم تنسيق الإخراج بشكل جميل حيثما كان ذلك ممكنًا. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | يُستدعى أثناء حفظ المستند ويقبل بيانات حول تقدم الحفظ. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. القيمة الافتراضية هي **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الموارد (الصور، الخطوط و css) عند تصدير مستند إلى تنسيق Html ثابت. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | يحدد المجلد الفعلي حيث تُحفظ الموارد (الصور، الخطوط، css) عند تصدير مستند إلى تنسيق Html. القيمة الافتراضية هي **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند Html. القيمة الافتراضية هي **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | العلم يشير إلى ما إذا كان يجب وضع قواعد CSS \"@font-face\" في ملف منفصل \"fontFaces.css\" عندما يتم حفظ المستند باستخدام ورقة أنماط خارجية (أي عندما يكون [ExportEmbeddedCss](./get_exportembeddedcss/) **false**). القيمة الافتراضية هي **false**، جميع قواعد CSS تُكتب في ملف واحد \"styles.css\". |
| [get_SaveFormat](./get_saveformat/)() override | يحدد التنسيق الذي سيُحفظ به المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | يحدد ما إذا كان يجب إظهار الحد حول الصفحات. القيمة الافتراضية هي **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | يحدد المجلد الخاص بالملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) يتم تحديثها قبل الحفظ. القيمة الافتراضية هي **false**؛. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | يحصل على قيمة تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند إلى صيغة صفحة ثابتة. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) يتم تحديثها قبل الحفظ. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) يتم تحديثها قبل الحفظ. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | يحصل على قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر التحكم OLE. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام مضاد التسنين في العرض أم لا. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | العلم يشير إلى ما إذا كان يجب استخدام الخطوط من الجهاز الهدف لعرض المستند. إذا تم ضبط هذا العلم إلى **true**, فإن خصائص [FontFormat](./get_fontformat/) و [ExportEmbeddedFonts](./get_exportembeddedfonts/) لا تأثير لها، كما أن [ResourceSavingCallback](./get_resourcesavingcallback/) لا يتم استدعاؤه للخطوط. القيمة الافتراضية هي **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | يضبط قيمة تحدد كيفية عرض الألوان. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | يحدد البادئة التي تُضاف إلى جميع أسماء الفئات في ملف style.css. القيمة الافتراضية هي **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | يضبط قيمة تحدد كيفية عرض تأثيرات الـ 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | مُعيّن لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | يضبط [NumeralFormat](../numeralformat/) المستخدم في عرض الأرقام. تُستخدم الأرقام الأوروبية افتراضيًا. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الموارد (الصور، الخطوط و css) عند تصدير مستند إلى تنسيق Html ثابت. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | يحدد التنسيق الذي سيُحفظ به المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | يحدد ما إذا كان يجب إظهار الحد حول الصفحات. القيمة الافتراضية هي **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | يضبط قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر تحكم OLE. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | دالة الضبط لـ [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
