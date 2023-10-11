---
title: Class Document
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Document فصل. يمثل مستند Word.
type: docs
weight: 430
url: /ar/net/aspose.words/document/
---
## Document class

يمثل مستند Word.

لمعرفة المزيد، قم بزيارة[العمل مع الوثيقة](https://docs.aspose.com/words/net/working-with-document/) مقالة توثيقية.

```csharp
public class Document : DocumentBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Document](document/#constructor)() | إنشاء مستند Word فارغ. |
| [Document](document/#constructor_1)(Stream) | فتح مستند موجود من الدفق. يكتشف تنسيق الملف تلقائيًا. |
| [Document](document/#constructor_3)(string) | فتح مستند موجود من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [Document](document/#constructor_2)(Stream, LoadOptions) | فتح مستند موجود من الدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |
| [Document](document/#constructor_4)(string, LoadOptions) | فتح مستند موجود من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | الحصول على أو تعيين المسار الكامل للقالب المرفق بالمستند. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | الحصول على أو تعيين علامة تشير إلى ما إذا كانت الأنماط الموجودة في المستند قد تم تحديثها لتتوافق مع الأنماط الموجودة في القالب المرفق في كل مرة يتم فيها فتح المستند في برنامج MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | الحصول على شكل خلفية المستند أو تعيينه. يمكن ان يكون`باطل` . |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | إرجاع مجموعة تمثل كافة خصائص المستند المضمنة في المستند. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | يوفر الوصول إلى خيارات توافق المستندات (أي تفضيلات المستخدم التي تم إدخالها في ملف **التوافق** علامة التبويب **خيارات** الحوار في Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | الحصول على إصدار توافق OOXML المحدد من محتوى المستند الذي تم تحميله. هذا منطقي فقط لمستندات OOXML. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأطفال المباشرين لهذه العقدة. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | إرجاع مجموعة تمثل كافة خصائص المستند المخصصة للمستند. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | الحصول على مجموعة أجزاء تخزين بيانات XML المخصصة أو تعيينها. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | الحصول على الفاصل الزمني (بالنقاط) أو تعيينه بين علامات الجدولة الافتراضية. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | الحصول على مجموعة التوقيعات الرقمية لهذه الوثيقة ونتائج التحقق من صحتها. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | يحصل على هذا المثيل. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | يوفر خيارات تتحكم في ترقيم التعليقات الختامية وموضعها في هذا المستند. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | يحصل على[`FieldOptions`](../../aspose.words.fields/fieldoptions/) الكائن الذي يمثل خيارات التحكم في معالجة الحقل في المستند. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على الطفل الأول للعقدة. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | للحصول على القسم الأول في المستند. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذا المستند. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | الحصول على إعدادات خط المستند أو تعيينها. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | يوفر خيارات تتحكم في ترقيم الحواشي السفلية وموضعها في هذا المستند. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | إرجاع أ[`Frameset`](./frameset/)على سبيل المثال، إذا كان هذا المستند يمثل صفحة إطارات. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | الحصول على مستند المسرد أو تعيينه داخل هذا المستند أو القالب. مستند المسرد عبارة عن وحدة تخزين لإدخالات النص التلقائي والتصحيح التلقائي وكتل البناء المحددة في المستند. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | إرجاع`حقيقي` إذا تم تدقيق المستند من الناحية النحوية. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | إرجاع`حقيقي` إذا كان المستند يحتوي على مشروع VBA (وحدات الماكرو). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | إرجاع`حقيقي` إذا كان المستند يحتوي على أي تغييرات متعقبة. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | يوفر الوصول إلى خيارات الواصلة في المستند. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | يحدد ما إذا كان سيتم تضمين مربعات النص والحواشي السفلية والتعليقات الختامية في إحصائيات عدد الكلمات. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` لأن هذه العقدة يمكن أن تحتوي على عقد فرعية. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | الحصول على أو تعيين ضبط تباعد الأحرف في المستند. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على الطفل الأخير للعقدة. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | للحصول على القسم الأخير في المستند. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | يحصل على[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) الكائن الذي يمثل خيارات للتحكم في عملية التخطيط لهذا المستند. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | يوفر الوصول إلى تنسيق القائمة المستخدم في المستند. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | إرجاع أ[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) الكائن الذي يمثل وظيفة دمج البريد للمستند. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | الحصول على الكائن الذي يحتوي على كافة معلومات دمج المراسلات لمستند أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | يتم استدعاؤه عند إدراج عقدة أو إزالتها في المستند. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | إرجاعDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | الحصول على اسم الملف الأصلي للمستند. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | الحصول على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | الحصول على أو تعيين مجموعة الأجزاء المخصصة (محتوى عشوائي) المرتبطة بحزمة OOXML باستخدام "علاقات غير معروفة". |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | الحصول على أو تعيين لون صفحة المستند. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | الحصول على عدد الصفحات في المستند كما تم حسابه بواسطة عملية تخطيط الصفحة الأخيرة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | للحصول على نوع حماية المستند النشط حاليًا. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | الحصول على أو تعيين علامة تشير إلى أن Microsoft Word سيقوم بإزالة كافة معلومات المستخدم من التعليقات والمراجعات و خصائص المستند عند حفظ المستند. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | الحصول على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا المستند. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم العمل مع النسخة الأصلية أو المنقحة من المستند. |
| [Sections](../../aspose.words/document/sections/) { get; } | إرجاع مجموعة تمثل كافة الأقسام في المستند. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | يحدد ما إذا كان سيتم تشغيل التظليل الرمادي في حقول النموذج. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | يحدد ما إذا كان سيتم عرض الأخطاء النحوية في هذا المستند. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | يحدد ما إذا كان سيتم عرض الأخطاء الإملائية في هذا المستند أم لا. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | إرجاع`حقيقي` إذا تم التدقيق الإملائي للمستند. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | إرجاع مجموعة من الأنماط المحددة في المستند. |
| [Theme](../../aspose.words/document/theme/) { get; } | يحصل على[`Theme`](./theme/) كائن لهذا المستند. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | صحيح إذا تم تعقب التغييرات عند تحرير هذا المستند في Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | إرجاع مجموعة المتغيرات المضافة إلى مستند أو قالب. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | الحصول على أو تعيين a[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | الحصول على عدد إصدارات المستند التي تم تخزينها في مستند DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | يوفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | يتم استدعاؤه أثناء إجراءات معالجة المستندات المختلفة عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | يوفر الوصول إلى العلامة المائية للمستند. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | إرجاع مجموعة تمثل قائمة بالوظائف الإضافية لجزء المهام. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | يوفر الوصول إلى خيارات الحماية ضد الكتابة في المستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(DocumentVisitor) | يقبل الزائر. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | قبول كافة التغييرات المتعقبة في المستند. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(Document, ImportFormatMode) | إلحاق المستند المحدد بنهاية هذا المستند. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | إلحاق المستند المحدد بنهاية هذا المستند. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | ينظف الأنماط والقوائم غير المستخدمة من المستند. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(CleanupOptions) | ينظف الأنماط والقوائم غير المستخدمة من المستند اعتمادًا على ما هو محدد[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | إجراء نسخة عميقة من ملف`Document` . |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [Compare](../../aspose.words/document/compare/#compare)(Document, string, DateTime) | يقارن هذا المستند بمستند آخر ينتج عنه تغييرات حسب عدد مراجعات التحرير والتنسيق[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(Document, string, DateTime, CompareOptions) | يقارن هذا المستند بمستند آخر ينتج عنه تغييرات بعدد من مراجعات التحرير والتنسيق[`Revision`](../revision/) . يسمح بتحديد خيارات المقارنة باستخدام[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(Document) | نسخ الأنماط من القالب المحدد إلى مستند. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(string) | نسخ الأنماط من القالب المحدد إلى مستند. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | إنشاء متصفح يمكن استخدامه لاجتياز العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | إذا كانت الوثيقة لا تحتوي على أقسام، قم بإنشاء قسم واحد بفقرة واحدة. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | تحويل التنسيق المحدد في أنماط الجدول إلى تنسيق مباشر على الجداول في المستند. |
| [ExtractPages](../../aspose.words/document/extractpages/)(int, int) | إرجاع`Document` كائن يمثل نطاقًا محددًا من الصفحات. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | إرجاع العقدة الفرعية N التي تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | إرجاع مجموعة مباشرة من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لتكرار كل نمط عبر العقد الفرعية لهذه العقدة. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(int) | للحصول على حجم الصفحة واتجاهها ومعلومات أخرى حول الصفحة التي قد تكون مفيدة للطباعة أو العرض. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | يستورد عقدة من مستند آخر إلى المستند الحالي. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار التحكم في التنسيق. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | يتم تشغيل عمليات الانضمام بنفس التنسيق في جميع فقرات المستند. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | تغيير قيم نوع الحقل[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في رموز الحقول. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Print](../../aspose.words/document/print/#print)() | طباعة المستند بالكامل إلى الطابعة الافتراضية. |
| [Print](../../aspose.words/document/print/#print_1)(PrinterSettings) | يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم). |
| [Print](../../aspose.words/document/print/#print_3)(string) | طباعة المستند بالكامل إلى الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم). |
| [Print](../../aspose.words/document/print/#print_2)(PrinterSettings, string) | يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم) واسم المستند. |
| [Protect](../../aspose.words/document/protect/#protect)(ProtectionType) | يحمي المستند من التغييرات دون تغيير كلمة المرور الحالية أو تعيين كلمة مرور عشوائية. |
| [Protect](../../aspose.words/document/protect/#protect_1)(ProtectionType, string) | يحمي المستند من التغييرات ويعين كلمة مرور الحماية بشكل اختياري. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | إزالة جميع العقد الفرعية للعقدة الحالية. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | إزالة مراجع مخطط XML الخارجية من هذا المستند. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | إزالة كافة وحدات الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/)العقد التابعة للعقدة الحالية. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(int, Graphics, float, float, float) | يعرض صفحة المستند إلى ملفGraphics كائن بمقياس محدد. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(int, Graphics, float, float, float, float) | يعرض صفحة المستند إلى ملفGraphics كائن بحجم محدد. |
| [Save](../../aspose.words/document/save/#save_2)(string) | يحفظ المستند في ملف. يحدد تنسيق الحفظ تلقائيًا من الامتداد. |
| [Save](../../aspose.words/document/save/#save)(Stream, SaveFormat) | يحفظ المستند في دفق باستخدام التنسيق المحدد. |
| [Save](../../aspose.words/document/save/#save_1)(Stream, SaveOptions) | يحفظ المستند في دفق باستخدام خيارات الحفظ المحددة. |
| [Save](../../aspose.words/document/save/#save_3)(string, SaveFormat) | يحفظ المستند في ملف بالتنسيق المحدد. |
| [Save](../../aspose.words/document/save/#save_4)(string, SaveOptions) | يحفظ المستند في ملف باستخدام خيارات الحفظ المحددة. |
| [Save](../../aspose.words/document/save/#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | يرسل المستند إلى متصفح العميل. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | تحديد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | تحديد الأول[`Node`](../node/) الذي يطابق تعبير XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(string) | يبدأ تلقائيًا بوضع علامة على كافة التغييرات الإضافية التي تجريها على المستند برمجيًا باعتبارها تغييرات مراجعة. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(string, DateTime) | يبدأ تلقائيًا بوضع علامة على كافة التغييرات الإضافية التي تجريها على المستند برمجيًا باعتبارها تغييرات مراجعة. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | إيقاف وضع العلامات التلقائية على تغييرات المستند كمراجعات. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | إلغاء ربط الحقول في المستند بأكمله. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | إزالة الحماية عن المستند بغض النظر عن كلمة المرور. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(string) | إزالة الحماية عن المستند إذا تم تحديد كلمة مرور صحيحة. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | يقوم بتحديث قيم الحقول في المستند بأكمله. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | تحديث تسميات القائمة لجميع عناصر القائمة في المستند. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | يعيد بناء تخطيط الصفحة للمستند. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | التحديثات[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) للمستند باستخدام الخيارات الافتراضية. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(ThumbnailGeneratingOptions) | التحديثات[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) للمستند حسب الخيارات المحددة. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | لتحديث خصائص عدد الكلمات في المستند. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(bool) | يقوم بتحديث خصائص عدد الكلمات في المستند، ويتم تحديثه بشكل اختياري[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) الملكية. |

### ملاحظات

ال`Document` هو كائن مركزي في مكتبة Aspose.Words.

لتحميل مستند موجود في أي من[`LoadFormat`](../loadformat/) التنسيقات، قم بتمرير ملف name أو دفق إلى أحد ملفات`Document`بناة. لإنشاء مستند فارغ، قم باستدعاء المُنشئ بدون معلمات.

استخدم إحدى عمليات التحميل الزائد لطريقة الحفظ لحفظ المستند في أي من [`SaveFormat`](../saveformat/) التنسيقات.

لرسم صفحات المستند مباشرةً على ملف **الرسومات** استخدام الكائن [`RenderToScale`](./rendertoscale/) أو[`RenderToSize`](./rendertosize/) طريقة.

لطباعة المستند، استخدم أحد[`Print`](./print/) طُرق.

[`MailMerge`](./mailmerge/) هو محرك تقارير Aspose.Words الذي يسمح بملء التقارير المصممة في Microsoft Word ببيانات من مصادر بيانات مختلفة بسرعة وسهولة. يمكن أن تكون البيانات من DataSet أو DataTable أو DataView أو IDataReader أو مجموعة من القيم.  **دمج المراسلات** سوف يقوم باستعراض السجلات الموجودة في مصدر البيانات وإدراجها في حقول دمج المراسلات في المستند والتي ستزيدها حسب الضرورة.

`Document` يقوم بتخزين معلومات على مستوى المستند مثل[`Styles`](../documentbase/styles/)[`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/)والقوائم ووحدات الماكرو. يمكن الوصول إلى معظم هذه الكائنات عبر الخصائص المقابلة لـ`Document`.

ال`Document` هي عقدة جذر لشجرة تحتوي على جميع العقد الأخرى للمستند. الشجرة عبارة عن نمط تصميم مركب وتشبه في العديد من النواحي XmlDocument. يمكن معالجة محتوى المستند بحرية برمجيًا:

* يمكن الوصول إلى عقد الوثيقة عبر المجموعات المكتوبة، على سبيل المثال[`Sections`](./sections/)[`ParagraphCollection`](../paragraphcollection/) إلخ.
* يمكن تحديد عقد الوثيقة حسب نوع العقدة الخاصة بها باستخدام [`GetChildNodes`](../compositenode/getchildnodes/) أو باستخدام استعلام XPath مع[`SelectNodes`](../compositenode/selectnodes/) أو[`SelectSingleNode`](../compositenode/selectsinglenode/).
* يمكن إضافة عقد المحتوى أو إزالتها من أي مكان في المستند باستخدام Node) ,Node)Node) وطرقother التي توفرها الفئة الأساسية[`CompositeNode`](../compositenode/).
* يمكن تغيير سمات التنسيق لكل عقدة عبر خصائص تلك العقدة.

فكر في استخدام[`DocumentBuilder`](../documentbuilder/)يؤدي ذلك إلى تبسيط مهمة إنشاء برمجيًا أو ملء شجرة المستندات.

ال`Document` يمكن أن تحتوي فقط[`Section`](../section/) أشياء.

في Microsoft Word، يجب أن يحتوي المستند الصالح على قسم واحد على الأقل.

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
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند واحد لدمج البريد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// إنشاء مستند مصدر لدمج البريد.
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

* class [DocumentBase](../documentbase/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


