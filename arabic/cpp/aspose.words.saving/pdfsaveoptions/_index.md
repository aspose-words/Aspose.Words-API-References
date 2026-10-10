---
title: "Aspose::Words::Saving::PdfSaveOptions class"
linktitle: "PdfSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions class. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند إلى تنسيق Pdf. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند بتنسيق [Pdf](../../aspose.words/saveformat/). لمعرفة المزيد، زر مقالة الوثائق [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | ينشئ نسخة عميقة من هذا الكائن. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | علامة تحدد ما إذا كان يجب كتابة عوامل تموضع النص الإضافية أم لا. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | يحصل أو يضبط قيمة تحدد كيفية تضمين المرفقات في مستند PDF. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان يجب تخزين الرسومات الموضوعة في خلفية المستند مؤقتًا أم لا. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | يحصل على قيمة تحدد كيفية عرض الألوان. |
| [get_Compliance](./get_compliance/)() const | يحدد مستوى التوافق مع معايير PDF للمستندات الناتجة. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | يحدد ما إذا كان يجب تحويل مراجع الحواشي/الحواشي الختامية في قصة النص الرئيسي إلى روابط تشعبية نشطة. عند النقر، سيؤدي الرابط إلى الحاشية/الحاشية الختامية المقابلة. القيمة الافتراضية هي **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | يحصل أو يضبط قيمة تحدد الطريقة التي يتم بها تصدير [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) إلى ملف PDF. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | يحصل أو يعيّن المنطقة الزمنية المحلية المخصصة المستخدمة في حقول التاريخ/الوقت. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | يحصل أو يضبط تفاصيل توقيع مستند PDF الناتج. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | علامة تحدد ما إذا كان شريط عنوان النافذة يجب أن يعرض عنوان المستند المأخوذ من إدخال Title في قاموس معلومات المستند. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | يحصل على قيمة تحدد كيفية عرض تأثيرات 3D. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | يحصل أو يعيّن قيمة تحدد كيفية عرض تأثيرات DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض أشكال DrawingML. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | يسمح بتحديد خيارات تقليل العينة. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | يحصل أو يضبط تفاصيل تشفير مستند PDF الناتج. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان يجب تصدير بنية المستند أم لا. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت الأشكال العائمة تُصدَّر كوسوم مضمنة في بنية المستند. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان يجب إنشاء وسم "Span" في بنية المستند لتصدير لغة النص أم لا. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان يجب وضع علامة على رسم الفقرة كعنصر غير أساسي. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | يحدد وضع تضمين الخط. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | يحدد ما إذا كان يجب إنشاء سكريبتات تحاكي سلوك حقول النماذج الخاصة بـ Microsoft Word في PDF. القيمة الافتراضية هي **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | يحدد كيفية تصدير العلامات المرجعية في رؤوس/تذييلات الصفحات. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | يحدد كيفية اختيار مساحة اللون للصور في مستند PDF. |
| [get_ImageCompression](./get_imagecompression/)() const | يحدد نوع الضغط الذي سيُستخدم لجميع الصور في المستند. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [get_InterpolateImages](./get_interpolateimages/)() const | علامة تشير إلى ما إذا كان يجب أن يقوم القارئ المتوافق بإجراء استيفاء الصورة. عندما يتم تحديد **false**، لا تُكتب العلامة إلى المستند الناتج ويُستخدم السلوك الافتراضي للقارئ بدلاً من ذلك. |
| [get_JpegQuality](./get_jpegquality/)() | يحصل أو يضبط قيمة تحدد جودة صور JPEG داخل مستند PDF. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | يحصل أو يضبط قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | يحصل على قيمة تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | يحصل على [NumeralFormat](../numeralformat/) المستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت الروابط التشعبية في مستند Pdf الناتج تُجبر على الفتح في نافذة جديدة (أو تبويب) في المتصفح. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | العلم يشير إلى ما إذا كان من الضروري تحسين الإخراج. إذا تم تعيين هذا العلم، تُزال القنوات المتداخلة الزائدة والقنوات الفارغة، كما يتم دمج الرموز المجاورة ذات التنسيق نفسه. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية إلى **true**. القيمة الافتراضية هي **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | يسمح بتحديد خيارات المخطط. |
| [get_PageLayout](./get_pagelayout/)() const | يحدد تخطيط الصفحة الذي سيُستخدم عند فتح المستند في قارئ PDF. |
| [get_PageMode](./get_pagemode/)() const | يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | يحصل أو يضبط الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند. |
| [get_PreblendImages](./get_preblendimages/)() const | يحصل أو يعيّن قيمة تحدد ما إذا كان يجب دمج الصور الشفافة مسبقًا مع لون الخلفية الأسود أم لا. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | يحدد ما إذا كان يجب الحفاظ على حقول نماذج Microsoft Word كحقول نماذج في PDF أو تحويلها إلى نص. القيمة الافتراضية هي **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | عند **true**، يتم تنسيق الإخراج بشكل جميل حيثما كان ذلك ممكنًا. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | يُستدعى أثناء حفظ المستند ويقبل بيانات حول تقدم الحفظ. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | يحدد ما إذا كان يجب عرض حد حقل اختيار نموذج PDF. |
| [get_SaveFormat](./get_saveformat/)() override | يحدد الصيغة التي سيتم حفظ المستند بها إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون فقط [Pdf](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | يحدد المجلد الخاص بالملفات المؤقتة المستخدمة عند الحفظ إلى ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية **null** ولا تُستخدم أي ملفات مؤقتة. |
| [get_TextCompression](./get_textcompression/)() const | يحدد نوع الضغط الذي سيُستخدم لجميع المحتويات النصية في المستند. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) يتم تحديثها قبل الحفظ. القيمة الافتراضية هي **false**؛. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | يحصل على قيمة تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند إلى صيغة صفحة ثابتة. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) يتم تحديثها قبل الحفظ. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | يحصل أو يضبط قيمة تحدد ما إذا كانت خاصية [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) يتم تحديثها قبل الحفظ. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | يحصل على قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر التحكم OLE. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام مضاد التسنين في العرض أم لا. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب، إذا تم تحديده عبر [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | يحصل أو يعيّن قيمة تحدد ما إذا كان يجب استبدال خطوط TrueType Arial و Times New Roman و Courier New و Symbol بخطوط PDF Type 1 الأساسية أم لا. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | يحصل أو يضبط قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | يحدد ما إذا كان يجب استخدام خاصية Tag أو Id في عنصر التحكم SDT كاسم لحقل النموذج في PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | يحصل على قيمة تحدد نوع التكبير الذي يجب تطبيقه عند فتح المستند باستخدام عارض PDF. |
| [get_ZoomFactor](./get_zoomfactor/)() const | يحصل على قيمة تحدد عامل التكبير (بالنسبة المئوية) للمستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | ينشئ مثيلًا جديدًا من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Pdf](../../aspose.words/saveformat/). |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | يضبط قيمة تحدد كيفية عرض الألوان. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | يحدد مستوى التوافق مع معايير PDF للمستندات الناتجة. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | يحدد ما إذا كان يجب تحويل مراجع الحواشي/الحواشي الختامية في قصة النص الرئيسي إلى روابط تشعبية نشطة. عند النقر، سيؤدي الرابط إلى الحاشية/الحاشية الختامية المقابلة. القيمة الافتراضية هي **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | يضبط قيمة تحدد كيفية عرض تأثيرات الـ 3D. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | يسمح بتحديد خيارات تقليل العينة. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | يسمح بتحديد خيارات عرض ملفات الميتا. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | يضبط [NumeralFormat](../numeralformat/) المستخدم في عرض الأرقام. تُستخدم الأرقام الأوروبية افتراضيًا. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | يحدد تخطيط الصفحة الذي سيُستخدم عند فتح المستند في قارئ PDF. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير المستند إلى تنسيق صفحة ثابتة. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | محدد لـ [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | يحدد الصيغة التي سيتم حفظ المستند بها إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون فقط [Pdf](../../aspose.words/saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | يضبط قيمة تحدد ما إذا كان سيتم تحديث صورة عرض عناصر تحكم OLE. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | محدد لـ [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | يحدد قيمة تحدد نوع التكبير الذي يجب تطبيقه عند فتح المستند باستخدام عارض PDF. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | يحدد قيمة تحدد عامل التكبير (بالنسبة المئوية) للمستند. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
