---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions class. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند إلى صيغ Html أو Mhtml أو Epub أو Azw3 أو Mobi. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند إلى صيغة [Html](../../aspose.words/saveformat/)، [Mhtml](../../aspose.words/saveformat/)، [Epub](../../aspose.words/saveformat/)، [Azw3](../../aspose.words/saveformat/) أو [Mobi](../../aspose.words/saveformat/). لمعرفة المزيد، زر مقالة الوثائق [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يُسمح بدمج الخطوط ذات المخططات PostScript عند دمج خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | يحدد ما إذا كانت الهوامش السالبة اليسرى واليمنى للفقرات تُعَدَّل عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | يحدد بادئة تُضاف إلى جميع أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة ولا تحتوي أسماء فئات CSS المُولدة على أي بادئة مشتركة. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | يسمح بالتحكم في كيفية حفظ أنماط CSS عندما يتم حفظ المستند إلى HTML أو MHTML أو EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | يحدد المسار واسم ورقة الأنماط المتدرجة [Style](../../aspose.words/style/) (CSS) التي تُكتب عندما يتم تصدير المستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | يحدد كيفية تصدير أنماط CSS (ورقة الأنماط المتدرجة [Style](../../aspose.words/style/)) إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [Inline](../cssstylesheettype/) لـ HTML/MHTML و[External](../cssstylesheettype/) لـ EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | يحصل أو يعيّن المنطقة الزمنية المحلية المخصصة المستخدمة في حقول التاريخ/الوقت. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | يحصل على قيمة تحدد كيفية عرض تأثيرات 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | يحصل أو يعيّن قيمة تحدد كيفية عرض تأثيرات DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض أشكال DrawingML. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | يسمح بالتحكم في كيفية حفظ أجزاء المستند عندما يتم حفظ المستند إلى HTML أو EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | يحدد كيفية تقسيم المستند عند الحفظ إلى تنسيق [Html](../../aspose.words/saveformat/)، [Epub](../../aspose.words/saveformat/) أو [Azw3](../../aspose.words/saveformat/). القيمة الافتراضية هي [None](../documentsplitcriteria/) لـ HTML و[HeadingParagraph](../documentsplitcriteria/) لـ EPUB وAZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | يحدد الحد الأقصى لمستوى العناوين التي يتم عندها تقسيم المستند. القيمة الافتراضية هي **%2**. |
| [get_Encoding](./get_encoding/)() const | يحدد الترميز المستخدم عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **new UTF8Encoding(false)** (UTF-8 بدون BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | يحدد ما إذا كان سيتم استخدام عناوين URL من نوع CID (Content-ID) للإشارة إلى الموارد (الصور، الخطوط، CSS) المتضمنة في مستندات MHTML. القيمة الافتراضية هي **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | يحدد ما إذا كان سيتم تصدير خصائص المستند المدمجة والمخصصة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | يتحكم في كيفية حفظ حقول النموذج المنسدلة إلى HTML أو MHTML. القيمة الافتراضية هي **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | يحدد ما إذا كان يجب تصدير موارد الخط إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | يحدد ما إذا كان يجب تضمين موارد الخطوط في HTML بترميز Base64. القيمة الافتراضية هي **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | يحدد كيفية إخراج رؤوس وتذييلات الصفحات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [PerSection](../exportheadersfootersmode/) لـ HTML/MHTML و[None](../exportheadersfootersmode/) لـ EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | يحدد ما إذا كانت الصور تُحفظ بتنسيق Base64 في HTML أو MHTML أو EPUB الناتج. القيمة الافتراضية هي **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | يحدد ما إذا كانت معلومات اللغة تُصدر إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | يتحكم في كيفية إخراج تسميات القوائم إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | يحدد ما إذا كانت هوامش الصفحة تُصدر إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | يحدد ما إذا كان إعداد الصفحة يتم تصديره إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | يحدد ما إذا كان يجب كتابة معلومات الجولة عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **true** لـ HTML و **false** لـ MHTML و EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | يتحكم فيما إذا كانت عقد [Shape](../../aspose.words.drawing/shape/) تُحوَّل إلى صور SVG عند الحفظ إلى HTML أو MHTML أو EPUB أو AZW3. القيمة الافتراضية هي **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | يتحكم في كيفية حفظ حقول نماذج إدخال النص إلى HTML أو MHTML. القيمة الافتراضية هي **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | يحدد ما إذا كان يجب كتابة أرقام الصفحات إلى جدول المحتويات عند حفظ HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | يحدد ما إذا كان يجب كتابة إعلان DOCTYPE عند الحفظ إلى HTML أو MHTML. عندما تكون **true**، يتم كتابة إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هي **false**. عند الحفظ إلى EPUB أو HTML5 ([Html5](../htmlversion/)) يتم دائمًا كتابة إعلان DOCTYPE. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | يتحكم في أي موارد الخط تحتاج إلى تقليص عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الخطوط عندما يتم حفظ المستند إلى HTML أو MHTML أو EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | يحدد المجلد الفعلي حيث تُحفظ الخطوط عند تصدير مستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | يحدد اسم المجلد المستخدم لإنشاء عناوين URI للخطوط المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_HtmlVersion](./get_htmlversion/)() const | يحدد نسخة معيار HTML التي يجب استخدامها عند حفظ المستند إلى HTML أو MHTML. القيمة الافتراضية هي [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | يسمح بالتحكم في كيفية حفظ الصور عندما يتم حفظ المستند إلى HTML أو MHTML أو EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | يحدد المجلد الفعلي حيث تُحفظ الصور عند تصدير مستند إلى صيغة HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | يحصل على قيمة تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | يحدد بأي تنسيق تُحفظ ملفات الميتا عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [Png](../htmlmetafileformat/)، مما يعني أن ملفات الميتا تُعرض كصور PNG نقطية. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | يحدد الحد الأقصى لمستوى العناوين التي تُملأ في خريطة التنقل عند التصدير إلى صيغ EPUB أو MOBI أو AZW3. القيمة الافتراضية هي **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | يتحكم في كيفية تصدير كائنات OfficeMath إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | عند **true**، يتم تنسيق الإخراج بشكل جميل حيثما كان ذلك ممكنًا. القيمة الافتراضية هي **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | يُستدعى أثناء حفظ المستند ويقبل بيانات حول تقدم الحفظ. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. القيمة الافتراضية هي **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | يحدد ما إذا كان يجب استبدال أحرف الشرطة المائلة الخلفية بعلامات الين. القيمة الافتراضية هي **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | يحدد ما إذا كان يتم حل أسماء عائلات الخط المستخدمة في المستند واستبدالها وفقًا لـ [FontSettings](../../aspose.words/document/get_fontsettings/) عند كتابتها في صيغ تعتمد على HTML. |
| [get_ResourceFolder](./get_resourcefolder/)() const | يحدد مجلدًا فعليًا حيث يتم حفظ جميع الموارد مثل الصور والخطوط وملفات CSS الخارجية عند تصدير المستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | يحدد اسم المجلد المستخدم لإنشاء عناوين URI لجميع الموارد المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة. |
| [get_SaveFormat](./get_saveformat/)() override | يحدد الصيغة التي سيتم حفظ المستند بها إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون [Html](../../aspose.words/saveformat/)، [Mhtml](../../aspose.words/saveformat/)، [Epub](../../aspose.words/saveformat/)، [Azw3](../../aspose.words/saveformat/) أو [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | يحدد ما إذا كانت الصور تُقاس بواسطة Aspose.Words إلى حجم الشكل المحدد عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | يتحكم في كيفية تصدير عرض الجداول والصفوف والخلايا إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [All](../htmlelementsizeoutputmode/). |
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
| [HtmlSaveOptions](./htmlsaveoptions/)() | ينشئ مثيلًا جديدًا من هذه الفئة يمكن استخدامه لحفظ مستند بصيغة [Html](../../aspose.words/saveformat/). |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | ينشئ مثيلًا جديدًا من هذه الفئة يمكن استخدامه لحفظ مستند بصيغة [Html](../../aspose.words/saveformat/)، [Mhtml](../../aspose.words/saveformat/)، [Epub](../../aspose.words/saveformat/)، [Azw3](../../aspose.words/saveformat/) أو [Mobi](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | مُعيّن القيمة لـ [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ أنماط CSS عندما يتم حفظ المستند إلى HTML أو MHTML أو EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | مُعيّن القيمة لـ [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | مُعيّن القيمة لـ [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | يضبط قيمة تحدد كيفية عرض تأثيرات الـ 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ أجزاء المستند عندما يتم حفظ المستند إلى HTML أو EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | مُعيّن لـ [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | مُعيّن لـ [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الخطوط عندما يتم حفظ المستند إلى HTML أو MHTML أو EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | يسمح بالتحكم في كيفية حفظ الصور عندما يتم حفظ المستند إلى HTML أو MHTML أو EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | يضبط القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | دالة ضبط لـ [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. القيمة الافتراضية هي **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | دالة ضبط لـ [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
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



يوضح كيفية استخدام ترميز محدد عند حفظ مستند إلى .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// استخدم كائن SaveOptions لتحديد الترميز للمستند الذي سنقوم بحفظه.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// بشكل افتراضي، سيحتوي مستند .epub الناتج على جميع محتوياته في جزء HTML واحد.
// معيار التقسيم يتيح لنا تقسيم المستند إلى عدة أجزاء HTML.
// سنحدد المعايير لتقسيم المستند إلى فقرات عناوين.
// هذا مفيد للقراء الذين لا يمكنهم قراءة ملفات HTML التي تتجاوز حجمًا معينًا.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// حدد أننا نريد تصدير خصائص المستند.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


يوضح كيفية تحديد المجلد لتخزين الصور المرتبطة بعد الحفظ إلى .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// حدد خيارًا لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## انظر أيضًا

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
