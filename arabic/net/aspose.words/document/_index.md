---
title: Document
second_title: Aspose.Words لمراجع .NET API
description: يمثل مستند Word .
type: docs
weight: 420
url: /ar/net/aspose.words/document/
---
## Document class

يمثل مستند Word .

```csharp
public class Document : DocumentBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Document](document#constructor)() | إنشاء مستند Word فارغ . |
| [Document](document#constructor_1)(Stream) | يفتح مستندًا موجودًا من دفق. يكتشف تنسيق الملف تلقائيًا. |
| [Document](document#constructor_3)(string) | يفتح وثيقة موجودة من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [Document](document#constructor_2)(Stream, LoadOptions) | يفتح مستندًا موجودًا من دفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [Document](document#constructor_4)(string, LoadOptions) | يفتح وثيقة موجودة من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate) { get; set; } | الحصول على أو تعيين المسار الكامل للقالب المرفق بالمستند. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles) { get; set; } | الحصول على علامة أو تعيينها تشير إلى ما إذا كانت الأنماط الموجودة في المستند قد تم تحديثها لمطابقة الأنماط الموجودة في القالب المرفق في كل مرة يتم فيها فتح المستند في MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | الحصول على أو تحديد شكل خلفية المستند. يمكن أن يكون فارغًا. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties) { get; } | إرجاع مجموعة تمثل كافة خصائص المستند المضمنة في المستند. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | يحصل على جميع العقد الفرعية الفورية لهذه العقدة. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions) { get; } | يوفر الوصول إلى خيارات توافق المستندات (أي تفضيلات المستخدم التي تم إدخالها في ملف **التوافق** من علامة التبويب **خيارات** مربع حوار في Word). |
| [Compliance](../../aspose.words/document/compliance) { get; } | الحصول على إصدار التوافق OOXML المحدد من محتوى المستند الذي تم تحميله. يكون منطقيًا فقط لمستندات OOXML . |
| [Count](../../aspose.words/compositenode/count) { get; } | الحصول على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties) { get; } | إرجاع مجموعة تمثل كافة خصائص المستند المخصصة. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص . |
| [CustomXmlParts](../../aspose.words/document/customxmlparts) { get; set; } | الحصول على مجموعة أجزاء تخزين بيانات XML المخصصة أو تعيينها. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop) { get; set; } | الحصول على أو تحديد الفاصل الزمني (بالنقاط) بين علامات الجدولة الافتراضية. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures) { get; } | الحصول على مجموعة التوقيعات الرقمية لهذا المستند ونتائج التحقق من صحتها. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions) { get; } | يوفر خيارات تتحكم في ترقيم وموضع التعليقات الختامية في هذا المستند. |
| [FieldOptions](../../aspose.words/document/fieldoptions) { get; } | يحصل على أ **FieldOptions**كائن يمثل خيارات للتحكم في معالجة الحقل في المستند. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | الحصول على الطفل الأول للعقدة . |
| [FirstSection](../../aspose.words/document/firstsection) { get; } | يحصل على القسم الأول في المستند. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند. |
| [FontSettings](../../aspose.words/document/fontsettings) { get; set; } | الحصول على إعدادات خط المستند أو تعيينها. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions) { get; } | يوفر خيارات تتحكم في ترقيم وتحديد مواضع الحواشي السفلية في هذا المستند. |
| [Frameset](../../aspose.words/document/frameset) { get; } | إرجاع أ[`Frameset`](./frameset)مثال إذا كان هذا المستند يمثل صفحة إطارات. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument) { get; set; } | الحصول على أو تحديد مستند المسرد في هذا المستند أو القالب. مستند قاموس المصطلحات هو storage لإدخالات النص التلقائي والتصحيح التلقائي و Building Block المحددة في المستند. |
| [GrammarChecked](../../aspose.words/document/grammarchecked) { get; set; } | عوائد **حقيقي** إذا تم فحص المستند من أجل القواعد. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | إرجاع صحيح إذا كانت هذه العقدة بها أي عقد فرعية. |
| [HasMacros](../../aspose.words/document/hasmacros) { get; } | عوائد **حقيقي** إذا كان المستند يحتوي على مشروع VBA (وحدات ماكرو) . |
| [HasRevisions](../../aspose.words/document/hasrevisions) { get; } | عوائد **حقيقي** إذا كان المستند يحتوي على أي تغييرات متعقبة. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions) { get; } | يوفر الوصول إلى خيارات الواصلة في المستند. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | إرجاع صحيح لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | الحصول على آخر تابع للعقدة . |
| [LastSection](../../aspose.words/document/lastsection) { get; } | يحصل على القسم الأخير في المستند. |
| [LayoutOptions](../../aspose.words/document/layoutoptions) { get; } | يحصل على أ **خيارات التخطيط** كائن يمثل خيارات للتحكم في عملية التخطيط لهذا المستند . |
| [Lists](../../aspose.words/documentbase/lists) { get; } | يوفر الوصول إلى تنسيق القائمة المستخدم في المستند. |
| [MailMerge](../../aspose.words/document/mailmerge) { get; } | إرجاع أ **دمج المراسلات** كائن يمثل وظيفة دمج المراسلات للمستند. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings) { get; set; } | الحصول على الكائن الذي يحتوي على كافة معلومات دمج المراسلات لمستند أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | يتم استدعائها عند إدراج عقدة أو إزالتها في المستند. |
| override [NodeType](../../aspose.words/document/nodetype) { get; } | عوائد **NodeType.Document** . |
| [OriginalFileName](../../aspose.words/document/originalfilename) { get; } | الحصول على اسم الملف الأصلي للمستند. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat) { get; } | الحصول على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts) { get; set; } | الحصول على أو تعيين مجموعة الأجزاء المخصصة (محتوى عشوائي) المرتبطة بحزمة OOXML باستخدام "علاقات غير معروفة". |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | الحصول على أو تحديد لون صفحة المستند. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../documentbase/backgroundshape) . |
| [PageCount](../../aspose.words/document/pagecount) { get; } | الحصول على عدد الصفحات في المستند كما تم حسابه بواسطة أحدث عملية تخطيط للصفحة. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [ProtectionType](../../aspose.words/document/protectiontype) { get; } | يحصل على نوع حماية المستند النشط حاليًا. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation) { get; set; } | الحصول على أو تعيين علامة تشير إلى أن Microsoft Word سيزيل كافة معلومات المستخدم من التعليقات والمراجعات وخصائص المستند عند حفظ المستند. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية. |
| [Revisions](../../aspose.words/document/revisions) { get; } | الحصول على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا المستند. |
| [RevisionsView](../../aspose.words/document/revisionsview) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم العمل مع النسخة الأصلية أو المنقحة من المستند. |
| [Sections](../../aspose.words/document/sections) { get; } | إرجاع مجموعة تمثل كافة الأقسام في المستند. |
| [ShadeFormData](../../aspose.words/document/shadeformdata) { get; set; } | يحدد ما إذا كان سيتم تشغيل التظليل الرمادي في حقول النموذج. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors) { get; set; } | تحديد ما إذا كان سيتم عرض الأخطاء النحوية في هذا المستند. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors) { get; set; } | يحدد ما إذا كان سيتم عرض الأخطاء الإملائية في هذا المستند. |
| [SpellingChecked](../../aspose.words/document/spellingchecked) { get; set; } | عوائد **حقيقي** إذا تم فحص المستند من أجل التدقيق الإملائي. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | إرجاع مجموعة من الأنماط المحددة في المستند. |
| [Theme](../../aspose.words/document/theme) { get; } | يحصل على ملف[`Theme`](./theme) كائن لهذه الوثيقة. |
| [TrackRevisions](../../aspose.words/document/trackrevisions) { get; set; } | **حقيقي** إذا تم تعقب التغييرات عند تحرير هذا المستند في Microsoft Word. |
| [Variables](../../aspose.words/document/variables) { get; } | إرجاع مجموعة المتغيرات المضافة إلى مستند أو قالب. |
| [VbaProject](../../aspose.words/document/vbaproject) { get; set; } | يحصل أو يحدد أ[`VbaProject`](./vbaproject) . |
| [VersionsCount](../../aspose.words/document/versionscount) { get; } | الحصول على عدد إصدارات المستند التي تم تخزينها في مستند DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions) { get; } | يوفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word . |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | يتم استدعاؤه أثناء إجراءات معالجة المستندات المختلفة عند اكتشاف مشكلة قد تؤدي إلى في البيانات أو فقدان الدقة في التنسيق . |
| [Watermark](../../aspose.words/document/watermark) { get; } | يوفر الوصول إلى العلامة المائية للمستند. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes) { get; } | إرجاع مجموعة تمثل قائمة الوظائف الإضافية لجزء المهام. |
| [WriteProtection](../../aspose.words/document/writeprotection) { get; } | يوفر الوصول إلى خيارات الحماية ضد الكتابة في المستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/document/accept)(DocumentVisitor) | يقبل الزائر . |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions)() | قبول كافة التغييرات المتعقبة في المستند. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة . |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument)(Document, ImportFormatMode) | إلحاق المستند المحدد بنهاية هذا المستند. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | إلحاق المستند المحدد بنهاية هذا المستند. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup)() | ينظف الأنماط والقوائم غير المستخدمة من المستند. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup_1)(CleanupOptions) | ينظف الأنماط والقوائم غير المستخدمة من المستند حسب المعطى[`CleanupOptions`](../cleanupoptions) . |
| [Clone](../../aspose.words/document/clone#clone)() | يقوم بإجراء نسخة عميقة من ملف[`Document`](../document) . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [Compare](../../aspose.words/document/compare#compare)(Document, string, DateTime) | يقارن هذا المستند بمستند آخر ينتج عنه تغييرات كعدد مراجعات التحرير والتنسيق[`Revision`](../revision) . |
| [Compare](../../aspose.words/document/compare#compare_1)(Document, string, DateTime, CompareOptions) | مقارنة هذا المستند بمستند آخر ينتج عنه تغييرات في صورة عدد من مراجعات التحرير والتنسيق[`Revision`](../revision) . يسمح بتحديد خيارات المقارنة باستخدام[`CompareOptions`](../../aspose.words.comparing/compareoptions) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate)(Document) | نسخ الأنماط من القالب المحدد إلى مستند. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate_1)(string) | نسخ الأنماط من القالب المحدد إلى مستند. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | محجوز لاستخدام النظام. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum)() | في حالة عدم احتواء المستند على أقسام ، يتم إنشاء قسم واحد به فقرة واحدة. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting)() | تحويل التنسيق المحدد في أنماط الجدول إلى تنسيق مباشر على الجداول في المستند. |
| [ExtractPages](../../aspose.words/document/extractpages)(int, int) | إرجاع ملف[`Document`](../document) كائن يمثل نطاقًا محددًا من الصفحات. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | إرجاع العقدة الفرعية رقم N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | يوفر دعمًا لكل تكرار نمط على العقد التابعة لهذه العقدة . |
| [GetPageInfo](../../aspose.words/document/getpageinfo)(int) | الحصول على حجم الصفحة والاتجاه والمعلومات الأخرى حول الصفحة التي قد تكون مفيدة للطباعة أو التقديم. |
| override [GetText](../../aspose.words/compositenode/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool) | يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool, ImportFormatMode) | يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية مع خيار للتحكم في التنسيق. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | يدخل العقدة المحددة مباشرة بعد العقدة المرجعية المحددة. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | يقوم بإدراج العقدة المحددة مباشرة قبل العقدة المرجعية المحددة. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting)() | يتم تشغيل الصلات بنفس التنسيق في كل فقرات المستند. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes)() | يغير قيم نوع الحقل[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype) من[`FieldStart`](../../aspose.words.fields/fieldstart) و[`FieldSeparator`](../../aspose.words.fields/fieldseparator) و[`FieldEnd`](../../aspose.words.fields/fieldend) في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في أكواد الحقول. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة . |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Print](../../aspose.words/document/print#print)() | طباعة المستند بالكامل على الطابعة الافتراضية. |
| [Print](../../aspose.words/document/print#print_1)(PrinterSettings) | طباعة المستند وفقًا لإعدادات الطابعة المحددة ، باستخدام وحدة تحكم الطباعة القياسية (بدون واجهة مستخدم). |
| [Print](../../aspose.words/document/print#print_3)(string) | اطبع المستند بالكامل على الطابعة المحددة ، باستخدام وحدة تحكم الطباعة القياسية (بدون واجهة مستخدم). |
| [Print](../../aspose.words/document/print#print_2)(PrinterSettings, string) | طباعة المستند وفقًا لإعدادات الطابعة المحددة ، باستخدام وحدة تحكم الطباعة القياسية (بدون واجهة مستخدم) واسم المستند. |
| [Protect](../../aspose.words/document/protect#protect)(ProtectionType) | يحمي المستند من التغييرات بدون تغيير كلمة المرور الحالية أو تخصيص كلمة مرور عشوائية. |
| [Protect](../../aspose.words/document/protect#protect_1)(ProtectionType, string) | يحمي المستند من التغييرات ويعين اختياريًا كلمة مرور للحماية. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | يزيل كافة العقد التابعة للعقدة الحالية. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | يزيل العقدة الفرعية المحددة . |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences)() | إزالة مراجع مخطط XML الخارجية من هذا المستند. |
| [RemoveMacros](../../aspose.words/document/removemacros)() | يزيل كافة وحدات الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag) العقد التابعة للعقدة الحالية. |
| [RenderToScale](../../aspose.words/document/rendertoscale)(int, Graphics, float, float, float) | يعرض صفحة مستند إلى ملفGraphics كائن لمقياس محدد . |
| [RenderToSize](../../aspose.words/document/rendertosize)(int, Graphics, float, float, float, float) | يعرض صفحة مستند إلى ملفGraphics كائن لحجم محدد . |
| [Save](../../aspose.words/document/save#save_2)(string) | يحفظ المستند في ملف. يحدد تلقائيًا تنسيق الحفظ من الامتداد. |
| [Save](../../aspose.words/document/save#save)(Stream, SaveFormat) | يحفظ المستند إلى دفق باستخدام التنسيق المحدد. |
| [Save](../../aspose.words/document/save#save_1)(Stream, SaveOptions) | يحفظ المستند في دفق باستخدام خيارات الحفظ المحددة. |
| [Save](../../aspose.words/document/save#save_3)(string, SaveFormat) | يحفظ المستند في ملف بالتنسيق المحدد. |
| [Save](../../aspose.words/document/save#save_4)(string, SaveOptions) | يحفظ المستند في ملف باستخدام خيارات الحفظ المحددة. |
| [Save](../../aspose.words/document/save#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | يرسل المستند إلى مستعرض العميل . |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | تحديد قائمة بالعقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | تحديد العقدة الأولى التي تطابق تعبير XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions)(string) | يبدأ تلقائيًا في وضع علامة على جميع التغييرات الإضافية التي تجريها على المستند برمجيًا عند تغيير المراجعة. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions_1)(string, DateTime) | يبدأ تلقائيًا في وضع علامة على جميع التغييرات الإضافية التي تجريها على المستند برمجيًا عند تغيير المراجعة. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions)() | إيقاف وضع العلامات التلقائية على تغييرات المستند كمراجعات. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| [UnlinkFields](../../aspose.words/document/unlinkfields)() | إلغاء ربط الحقول في المستند بأكمله. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect_1)() | يزيل الحماية من المستند بغض النظر عن كلمة المرور. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect)(string) | يزيل الحماية من المستند إذا تم تحديد كلمة مرور صحيحة. |
| [UpdateFields](../../aspose.words/document/updatefields)() | يقوم بتحديث قيم الحقول في المستند بأكمله. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels)() | تحديث تسميات القائمة لكافة عناصر القائمة في المستند. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout)() | يعيد إنشاء تخطيط صفحة المستند. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail)() | التحديثات[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) من المستند باستخدام الخيارات الافتراضية. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail_1)(ThumbnailGeneratingOptions) | التحديثات[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) من المستند وفقًا للخيارات المحددة. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount)() | يقوم بتحديث خصائص عدد الكلمات الخاصة بالمستند. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount_1)(bool) | يحدّث خصائص عدد الكلمات في المستند ، ويتم تحديثه اختياريًا[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines) الملكية . |

### ملاحظات

ال **وثيقة** هو كائن مركزي في مكتبة Aspose.Words.

لتحميل مستند موجود في أي ملف[`LoadFormat`](../loadformat) ، قم بتمرير ملف name أو دفق إلى أحد ملفات **وثيقة** الصانعين. لإنشاء مستند فارغ ، اتصل بـ المُنشئ بدون معلمات.

استخدم أحد طرق الحفظ الزائد لحفظ المستند في أي من [`SaveFormat`](../saveformat) التنسيقات.

لرسم صفحات الوثيقة مباشرة على ملف **الرسومات** كائن use [`RenderToScale`](./rendertoscale) أو[`RenderToSize`](./rendertosize) طريقة.

لطباعة المستند ، استخدم أحد ملفات[`Print`](./print)طُرق.

[`MailMerge`](./mailmerge) هو محرك تقارير Aspose.Words الذي يسمح بملء_ التقارير المصممة في Microsoft Word ببيانات من مصادر بيانات مختلفة بسرعة وسهولة . يمكن أن تكون البيانات من DataSet أو DataTable أو DataView أو IDataReader أو مجموعة من القيم .  **دمج المراسلات** سوف يمر عبر السجلات الموجودة في مصدر البيانات وإدراجها في حقول دمج المراسلات في المستند التي تزداد حسب الضرورة.

**وثيقة** يخزن المعلومات على مستوى المستند مثل[`Styles`](../documentbase/styles) ، [`BuiltInDocumentProperties`](./builtindocumentproperties) و[`CustomDocumentProperties`](./customdocumentproperties) والقوائم ووحدات الماكرو. يمكن الوصول إلى معظم هذه الكائنات عبر الخصائص المقابلة لـ **وثيقة**.

ال **وثيقة**هي عقدة جذرية لشجرة تحتوي على جميع العقد الأخرى للوثيقة. الشجرة هي نمط تصميم مركب وتشبه من نواح كثيرة XmlDocument. يمكن معالجة محتوى المستند بحرية برمجيًا:

* يمكن الوصول إلى عقد المستند عبر المجموعات المكتوبة ، على سبيل المثال[`Sections`](./sections) ، [`ParagraphCollection`](../paragraphcollection) إلخ.
* يمكن تحديد عقد المستند حسب نوع العقدة باستخدام [`GetChildNodes`](../compositenode/getchildnodes) أو استخدام استعلام XPath مع[`SelectNodes`](../compositenode/selectnodes) أو[`SelectSingleNode`](../compositenode/selectsinglenode).
* يمكن إضافة عُقد المحتوى أو إزالتها من أي مكان في المستند باستخدام [`InsertBefore`](../compositenode/insertbefore) و[`InsertAfter`](../compositenode/insertafter) ، [`RemoveChild`](../compositenode/removechild) و other التي توفرها الفئة الأساسية[`CompositeNode`](../compositenode).
* يمكن تغيير سمات التنسيق لكل عقدة عبر خصائص تلك العقدة.

فكر في استخدام[`DocumentBuilder`](../documentbuilder) يبسط مهمة إنشاء برمجيًا أو ملء شجرة المستند.

ال **وثيقة** يمكن أن تحتوي فقط[`Section`](../section) أشياء.

في Microsoft Word ، يجب أن يحتوي المستند الصالح على قسم واحد على الأقل.

### أمثلة

يوضح كيفية تنفيذ دمج البريد مع البيانات من DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام DataTable كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريد ناتج واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريد ناتج واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// ينشئ مستند مصدر لدمج المراسلات.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### أنظر أيضا

* class [DocumentBase](../documentbase)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
