---
title: "فئة Aspose::Words::Document"
linktitle: "المستند"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Document. تمثل مستند Word. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words/document/
---
## Document class


يمثل مستند Word. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [AcceptAllRevisions](./acceptallrevisions/)() | يقبل جميع التغييرات المتتبعة في المستند. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة نهاية المستند. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا لزيارة بداية المستند. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | يضيف المستند المحدد إلى نهاية هذا المستند. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يضيف المستند المحدد إلى نهاية هذا المستند. |
| [Cleanup](./cleanup/)() | ينظف الأنماط والقوائم غير المستخدمة من المستند. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | ينظف الأنماط والقوائم غير المستخدمة من المستند بناءً على [CleanupOptions](../cleanupoptions/). |
| [Clone](./clone/)() | ينفذ نسخة عميقة من [Document](./). |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | يقارن هذا المستند بمستند آخر وينتج تغييرات على شكل عدد من تعديلات التحرير وتنسيق المراجعات [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن هذا المستند بمستند آخر وينتج تغييرات على شكل عدد من تعديلات التحرير وتنسيق المراجعات [Revision](../revision/). يسمح بتحديد خيارات المقارنة باستخدام [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | ينسخ الأنماط من القالب المحدد إلى مستند. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | ينسخ الأنماط من القالب المحدد إلى مستند. |
| [Document](./document/)() | ينشئ مستند Word فارغ. |
| [Document](./document/)(const System::String\&) | يفتح مستندًا موجودًا من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يفتح مستندًا موجودًا من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | يفتح مستندًا موجودًا من تدفق. يكتشف تنسيق الملف تلقائيًا. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يفتح مستندًا موجودًا من تدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | إذا لم يحتوي المستند على أقسام، ينشئ قسمًا واحدًا مع فقرة واحدة. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | يحول التنسيق المحدد في أنماط الجداول إلى تنسيق مباشر على الجداول في المستند. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | يعيد كائن [Document](./) الذي يمثل النطاق المحدد من الصفحات وخيارات استخراج الصفحات المعطاة. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | يعيد كائن [Document](./) الذي يمثل النطاق المحدد من الصفحات. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | يحصل أو يعيّن المسار الكامل للقالب المرفق بالمستند. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | يحصل أو يعيّن علامة تشير إلى ما إذا كانت الأنماط في المستند تُحدّث لتطابق الأنماط في القالب المرفق في كل مرة يُفتح فيها المستند في MS Word. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | يحصل أو يضبط شكل الخلفية للمستند. يمكن أن يكون **null**. |
| [get_Bibliography](./get_bibliography/)() | يحصل على كائن [Bibliography](./get_bibliography/) الذي يمثل قائمة المصادر المتاحة في المستند. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | يعيد مجموعة تمثل جميع خصائص المستند المدمجة في المستند. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | يوفر الوصول إلى خيارات توافق المستند (أي تفضيلات المستخدم المدخلة في علامة تبويب **Compatibility** من مربع حوار **Options** في Word). |
| [get_Compliance](./get_compliance/)() | يحصل على نسخة توافق OOXML المحددة من محتوى المستند المحمَّل. لا معنى لها إلا في مستندات OOXML. |
| [get_Count](../compositenode/get_count/)() | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | يعيد مجموعة تمثل جميع خصائص المستند المخصصة للمستند. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | يحصل أو يضبط مجموعة أجزاء تخزين بيانات XML المخصصة. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | يحصل أو يضبط الفاصل (بالنقاط) بين نقاط التبويب الافتراضية. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | يحصل على مجموعة التوقيعات الرقمية لهذا المستند ونتائج التحقق منها. |
| [get_Document](../documentbase/get_document/)() const override | يحصل على هذا الكائن. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | يوفر خيارات تتحكم في ترقيم وتحديد موضع الحواشي الختامية في هذا المستند. |
| [get_FieldOptions](./get_fieldoptions/)() | يحصل على كائن [FieldOptions](../../aspose.words.fields/fieldoptions/) الذي يمثل خيارات التحكم في معالجة الحقول في المستند. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | يحصل على الطفل الأول للعقدة. |
| [get_FirstSection](./get_firstsection/)() | يحصل على القسم الأول في المستند. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند. |
| [get_FontSettings](./get_fontsettings/)() const | يحصل أو يضبط إعدادات خط المستند. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | يوفر خيارات تتحكم في ترقيم وتحديد موضع الحواشي السفلية في هذا المستند. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | يوفر الوصول إلى فواصل الحواشي السفلية/الختامية المعرفة في المستند. |
| [get_Frameset](./get_frameset/)() const | يعيد كائن [Frameset](./get_frameset/) إذا كان هذا المستند يمثل صفحة إطارات. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | يحصل أو يضبط مستند القاموس داخل هذا المستند أو القالب. مستند القاموس هو مساحة تخزين لإدخالات AutoText و AutoCorrect و Building Block المعرفة في المستند. |
| [get_GrammarChecked](./get_grammarchecked/)() | يعيد **true** إذا تم فحص المستند للنحو. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | يرجع **true** إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [get_HasMacros](./get_hasmacros/)() | يعيد **true** إذا كان للمستند مشروع VBA (ماكرو). |
| [get_HasRevisions](./get_hasrevisions/)() | يعيد **true** إذا كان للمستند أي تغييرات متتبعة. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | يوفر الوصول إلى خيارات تجزئة الكلمات في المستند. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | يحدد ما إذا كان يجب تضمين مربعات النص والحواشي السفلية والختامية في إحصاءات عدد الكلمات. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | يرجع **true** لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [get_JustificationMode](./get_justificationmode/)() | يحصل أو يضبط تعديل تباعد الأحرف في المستند. |
| [get_LastChild](../compositenode/get_lastchild/)() const | يحصل على الطفل الأخير للعقدة. |
| [get_LastSection](./get_lastsection/)() | يحصل على القسم الأخير في المستند. |
| [get_LayoutOptions](./get_layoutoptions/)() const | يحصل على كائن [LayoutOptions](../../aspose.words.layout/layoutoptions/) يمثل الخيارات للتحكم في عملية تخطيط هذا المستند. |
| [get_Lists](../documentbase/get_lists/)() const | يوفر الوصول إلى تنسيق القوائم المستخدم في المستند. |
| [get_MailMerge](./get_mailmerge/)() | يرجع كائن [MailMerge](../../aspose.words.mailmerging/mailmerge/) يمثل وظيفة دمج البريد للمستند. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | يحصل على أو يضبط الكائن الذي يحتوي على جميع معلومات دمج البريد للمستند. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | يُستدعى عندما يتم إدراج عقدة أو إزالتها في المستند. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | يحصل على اسم الملف الأصلي للمستند. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | يحصل على تنسيق المستند الأصلي الذي تم تحميله إلى هذا الكائن. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | يحصل على أو يضبط مجموعة الأجزاء المخصصة (محتوى تعسفي) المرتبطة بحزمة OOXML باستخدام \"علاقات غير معروفة\". |
| [get_PageColor](../documentbase/get_pagecolor/)() | يحصل على أو يضبط لون صفحة المستند. هذه الخاصية هي نسخة أبسط من [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | يحصل على عدد الصفحات في المستند كما تم حسابه بواسطة أحدث عملية تخطيط للصفحة. |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | يحصل على نوع حماية المستند النشط حاليًا. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | يحدد ما إذا كان التباعد بين الحروف (kerning) يطبق على النص اللاتيني وعلامات الترقيم. |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | يوفر معلومات عن درجة قابلية القراءة للمستند. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | يحصل على أو يضبط علامة تشير إلى أن Microsoft Word سيزيل جميع معلومات المستخدم من التعليقات والمراجعات وخصائص المستند عند حفظ المستند. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | يسمح بالتحكم في طريقة تحميل الموارد الخارجية. |
| [get_Revisions](./get_revisions/)() | يحصل على مجموعة من المراجعات (التغييرات المتتبعة) الموجودة في هذا المستند. |
| [get_RevisionsView](./get_revisionsview/)() const | يحصل على أو يضبط قيمة تشير إلى ما إذا كان سيتم العمل بالإصدار الأصلي أو المعدل من المستند. |
| [get_Sections](./get_sections/)() | يرجع مجموعة تمثل جميع الأقسام في المستند. |
| [get_ShadeFormData](./get_shadeformdata/)() | يحدد ما إذا كان سيتم تشغيل التظليل الرمادي على حقول النموذج. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | يحدد ما إذا كان سيتم عرض أخطاء القواعد النحوية في هذا المستند. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | يحدد ما إذا كان سيتم عرض أخطاء الإملاء في هذا المستند. |
| [get_SpellingChecked](./get_spellingchecked/)() | يرجع **true** إذا تم فحص المستند للإملاء. |
| [get_Styles](../documentbase/get_styles/)() const | يرجع مجموعة من الأنماط المعرفة في المستند. |
| [get_Theme](./get_theme/)() | يحصل على كائن [Theme](./get_theme/) لهذا المستند. |
| [get_TrackRevisions](./get_trackrevisions/)() | صحيح إذا تم تتبع التغييرات عندما يتم تحرير هذا المستند في Microsoft Word. |
| [get_Variables](./get_variables/)() | يعيد مجموعة المتغيرات المضافة إلى مستند أو قالب. |
| [get_VbaProject](./get_vbaproject/)() const | يحصل أو يضبط [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | يحصل على عدد إصدارات المستند التي تم تخزينها في مستند DOC. |
| [get_ViewOptions](./get_viewoptions/)() | يوفر خيارات للتحكم في طريقة عرض المستند في Microsoft Word. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | يُستدعى أثناء إجراءات معالجة المستند المختلفة عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [get_Watermark](./get_watermark/)() | يوفر الوصول إلى علامة مائية المستند. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | يعيد مجموعة تمثل قائمة إضافات لوحة المهام. |
| [get_WriteProtection](./get_writeprotection/)() | يوفر الوصول إلى خيارات حماية الكتابة للمستند. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | يرجع عقدة الطفل رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../compositenode/getenumerator/)() override | يوفر دعمًا لتكرار نمط foreach على العقد الفرعية لهذا العقد. |
| [GetPageInfo](./getpageinfo/)(int32_t) | يحصل على حجم الصفحة واتجاهها ومعلومات أخرى حول الصفحة قد تكون مفيدة للطباعة أو العرض. |
| [GetText](../compositenode/gettext/)() override | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يستورد عقدة من مستند آخر إلى المستند الحالي. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | يجمع المقاطع ذات التنسيق نفسه في جميع فقرات المستند. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | يغيّر قيم نوع الحقل [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) لـ [FieldStart](../../aspose.words.fields/fieldstart/)، [FieldSeparator](../../aspose.words.fields/fieldseparator/)، [FieldEnd](../../aspose.words.fields/fieldend/) في كامل المستند بحيث تتطابق مع أنواع الحقول الموجودة في رموز الحقول. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | يحمي المستند من التغييرات دون تغيير كلمة المرور الحالية أو يعيّن كلمة مرور عشوائية. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | يحمي المستند من التغييرات ويحدد اختياريًا كلمة مرور الحماية. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveBlankPages](./removeblankpages/)() | يزيل الصفحات الفارغة من المستند. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | يزيل تخصيصات شريط الأدوات وأوامر لوحة المفاتيح من المستند. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | يزيل مراجع مخطط XML الخارجية من هذا المستند. |
| [RemoveMacros](./removemacros/)() | يزيل جميع الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | يزيل جميع العقد التابعة لـ [SmartTag](../../aspose.words.markup/smarttag/) للعقدة الحالية. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | يرسم صفحة المستند في كائن **Graphics** إلى مقياس محدد. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | يرسم صفحة المستند في كائن **Graphics** إلى حجم محدد. |
| [Save](./save/)(const System::String\&) | يحفظ المستند إلى ملف. يحدد تنسيق الحفظ تلقائيًا من الامتداد. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | يحفظ المستند إلى ملف بالتنسيق المحدد. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يحفظ المستند إلى ملف باستخدام خيارات الحفظ المحددة. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يحفظ المستند إلى تدفق باستخدام التنسيق المحدد. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يحفظ المستند إلى تدفق باستخدام خيارات الحفظ المحددة. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | يختار قائمة من العقد التي تطابق تعبير XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | يختار أول [Node](../node/) يطابق تعبير XPath. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | مُعيّن لـ [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | مُعيّن لـ [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | مُعيّن لـ [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | مُعيّن لـ [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | مُعيّن لـ [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | مُعيّن لـ [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | مُعيّن لـ [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | يُستدعى عندما يتم إدراج عقدة أو إزالتها في المستند. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | مُعيّن لـ [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | يسمح بالتحكم في طريقة تحميل الموارد الخارجية. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | مُعيّن لـ [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | مُعيّن لـ [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | مُعيّن لـ [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | المُعيّن لـ [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | يبدأ تلقائيًا بوضع علامة على جميع التغييرات اللاحقة التي تُجريها على المستند برمجيًا كالتغييرات المراجعية. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | يبدأ تلقائيًا بوضع علامة على جميع التغييرات اللاحقة التي تُجريها على المستند برمجيًا كالتغييرات المراجعية. |
| [StopTrackRevisions](./stoptrackrevisions/)() | يوقف وضع العلامة التلقائي على تغييرات المستند كمراجعات. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | يفك ارتباط الحقول في كامل المستند. |
| [Unprotect](./unprotect/)() | يزيل الحماية من المستند بغض النظر عن كلمة المرور. |
| [Unprotect](./unprotect/)(const System::String\&) | يزيل الحماية من المستند إذا تم تحديد كلمة مرور صحيحة. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | يحدّث خاصية [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) لجميع الحواشي السفلية والنهائية في المستند. |
| [UpdateFields](./updatefields/)() | يحدّث قيم الحقول في كامل المستند. |
| [UpdateListLabels](./updatelistlabels/)() | يحدّث تسميات القوائم لجميع عناصر القائمة في المستند. |
| [UpdatePageLayout](./updatepagelayout/)() | يعيد بناء تخطيط الصفحات للمستند. |
| [UpdateTableLayout](./updatetablelayout/)() | يطبق نهجًا سابقًا لإعادة حساب عرض أعمدة الجدول الذي يحتوي على مشكلات معروفة. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | يحدّث [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) للمستند وفقًا للخيارات المحددة. |
| [UpdateThumbnail](./updatethumbnail/)() | يحدّث [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) للمستند باستخدام الخيارات الافتراضية. |
| [UpdateWordCount](./updatewordcount/)() | يحدّث خصائص عدد الكلمات في المستند. |
| [UpdateWordCount](./updatewordcount/)(bool) | يحدّث خصائص عدد الكلمات في المستند، ويحدّث اختياريًا خاصية [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/). |
## ملاحظات


الـ [Document](./) هو كائن مركزي في مكتبة Aspose.Words.

لتحميل مستند موجود بأي من صيغ [LoadFormat](../loadformat/)، مرّر اسم ملف أو تدفق إلى أحد مُنشئي الـ [Document](./). لإنشاء مستند فارغ، استدعِ المُنشئ دون معلمات.

استخدم أحد إصدارات طريقة Save لحفظ المستند بأي من صيغ [SaveFormat](../saveformat/).

لرسم صفحات المستند مباشرةً على كائن **Graphics** استخدم طريقة [RenderToScale()](../) أو [RenderToSize()](../).

لطباعة المستند، استخدم أحد طرق [Print()](../).

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

الـ [Document](./) هو عقدة جذر لشجرة تحتوي على جميع العقد الأخرى في المستند. الشجرة هي نمط تصميم Composite وتتشابه في نواحٍ كثيرة مع XmlDocument. يمكن التلاعب بمحتوى المستند بحرية برمجيًا:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



فكّر في استخدام [DocumentBuilder](../documentbuilder/) الذي يبسط مهمة إنشاء أو تعبئة شجرة المستند برمجيًا.

الـ [Document](./) يمكنه احتواء كائنات [Section](../section/) فقط.

في Microsoft Word، يجب أن يحتوي المستند الصالح على قسم واحد على الأقل.
## انظر أيضًا

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
