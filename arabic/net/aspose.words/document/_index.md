---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Document لمعالجة مستندات Word بسلاسة. حسّن مشاريعك بميزات فعّالة وسهولة في التكامل.
type: docs
weight: 640
url: /ar/net/aspose.words/document/
---
## Document class

يمثل مستند Word.

لمعرفة المزيد، قم بزيارة[العمل مع المستند](https://docs.aspose.com/words/net/working-with-document/) مقالة توثيقية.

```csharp
public class Document : DocumentBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Document](document/#constructor)() | ينشئ مستند Word فارغًا. |
| [Document](document/#constructor_1)(*Stream*) | يفتح مستندًا موجودًا من مصدر. يكتشف تنسيق الملف تلقائيًا. |
| [Document](document/#constructor_3)(*string*) | يفتح مستندًا موجودًا من ملف. يكتشف تنسيق الملف تلقائيًا. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يفتح مستندًا موجودًا من مصدر. يسمح بتحديد خيارات إضافية، مثل كلمة مرور التشفير. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يفتح مستندًا موجودًا من ملف. يسمح بتحديد خيارات إضافية، مثل كلمة مرور التشفير. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | يحصل على المسار الكامل للقالب المرفق بالمستند أو يعينه. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كانت الأنماط في المستند يتم تحديثها لتتوافق مع الأنماط الموجودة في القالب المرفق في كل مرة يتم فيها فتح المستند في MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | يحصل على شكل خلفية المستند أو يضبطه. يمكن استخدامه`باطل` . |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | يحصل على[`Bibliography`](./bibliography/)الكائن الذي يمثل قائمة المصادر المتوفرة في المستند. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | يعيد مجموعة تمثل جميع خصائص المستند المضمنة. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | يوفر الوصول إلى خيارات توافق المستندات (أي تفضيلات المستخدم المدخلة على**التوافق** علامة التبويب من**خيارات**الحوار في Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | يحصل على إصدار التوافق مع OOXML المحدد من محتوى المستند المحمّل. يكون منطقيًا فقط بالنسبة لمستندات OOXML. |
| [Count](../../aspose.words/compositenode/count/) { get; } | يحصل على عدد الأبناء المباشرين لهذه العقدة. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | يعيد مجموعة تمثل جميع خصائص المستند المخصصة للمستند. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | يحصل على مجموعة أجزاء تخزين بيانات XML المخصصة أو يعينها. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | يحصل على الفاصل الزمني (بالنقاط) بين علامات التبويب الافتراضية أو يعينه. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | يحصل على مجموعة التوقيعات الرقمية لهذه الوثيقة ونتائج التحقق منها. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | يحصل على هذه المثيل. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | يوفر خيارات للتحكم في ترقيم وموضع الحواشي الختامية في هذا المستند. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | يحصل على[`FieldOptions`](../../aspose.words.fields/fieldoptions/) كائن يمثل خيارات للتحكم في التعامل مع الحقول في المستند. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | يحصل على أول طفل للعقدة. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | يحصل على القسم الأول في المستند. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | يوفر الوصول إلى خصائص الخطوط المستخدمة في هذه الوثيقة. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | يحصل على إعدادات خط المستند أو يعينها. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | يوفر خيارات للتحكم في ترقيم الحواشي السفلية وتحديد موقعها في هذا المستند. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | يوفر الوصول إلى فواصل الحواشي السفلية/النهائية المحددة في المستند. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | يعيد[`Frameset`](./frameset/) مثال إذا كانت هذه الوثيقة تمثل صفحة إطارات. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | يحصل على أو يعيّن مستند المصطلحات داخل هذا المستند أو القالب. مستند المصطلحات هو مخزن لإدخالات النص التلقائي والتصحيح التلقائي وكتل البناء المحددة في مستند. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | إرجاع`حقيقي` إذا تم التحقق من القواعد النحوية للمستند. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة تحتوي على أي عقد فرعية. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | إرجاع`حقيقي` إذا كان المستند يحتوي على مشروع VBA (ماكرو). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | إرجاع`حقيقي` إذا كان المستند يحتوي على أي تغييرات متعقبة. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | يوفر الوصول إلى خيارات وضع علامات الوصل في المستند. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | يحدد ما إذا كان سيتم تضمين مربعات النص والحواشي السفلية والختامية في إحصائيات عدد الكلمات. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | إرجاع`حقيقي` حيث يمكن لهذه العقدة أن تحتوي على عقد فرعية. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | يحصل على تعديل المسافة بين أحرف المستند أو يعينه. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | يحصل على آخر طفل للعقدة. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | يحصل على القسم الأخير في المستند. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | يحصل على[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) الكائن الذي يمثل الخيارات للتحكم في عملية تخطيط هذا المستند. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | يوفر الوصول إلى تنسيق القائمة المستخدم في المستند. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | يعيد[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) الكائن الذي يمثل وظيفة دمج البريد للمستند. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | يحصل على الكائن الذي يحتوي على كافة معلومات دمج البريد لمستند أو يعينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | يتم استدعاؤها عند إدراج عقدة أو إزالتها في المستند. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | إرجاعDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | يحصل على اسم الملف الأصلي للمستند. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | يحصل على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | يحصل على مجموعة الأجزاء المخصصة (المحتوى التعسفي) المرتبطة بحزمة OOXML باستخدام "علاقات غير معروفة" أو يعينها. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | يُحدِّد لون صفحة المستند أو يُحدِّده. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | يحصل على عدد الصفحات في المستند كما تم حسابه بواسطة عملية تخطيط الصفحة الأخيرة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | يحصل على نوع حماية المستند النشط حاليًا. |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | يحدد ما إذا كان التباعد بين الأحرف ينطبق على كل من النص اللاتيني وعلامات الترقيم. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | يحصل على أو يعين علمًا يشير إلى أن Microsoft Word سيقوم بإزالة جميع معلومات المستخدم من التعليقات والمراجعات وخصائص المستند عند حفظ المستند. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | يحصل على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا المستند. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم العمل مع الإصدار الأصلي أو المنقح للمستند. |
| [Sections](../../aspose.words/document/sections/) { get; } | يعيد مجموعة تمثل جميع الأقسام في المستند. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | يحدد ما إذا كان سيتم تشغيل التظليل الرمادي على حقول النموذج. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | يحدد ما إذا كان سيتم عرض أخطاء القواعد النحوية في هذا المستند. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | يحدد ما إذا كان سيتم عرض الأخطاء الإملائية في هذا المستند. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | إرجاع`حقيقي` إذا تم التحقق من صحة التهجئة في المستند. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | يعيد مجموعة من الأنماط المحددة في المستند. |
| [Theme](../../aspose.words/document/theme/) { get; } | يحصل على[`Theme`](./theme/) كائن لهذه الوثيقة. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | صحيح إذا تم تعقب التغييرات عند تحرير هذا المستند في Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | يعيد مجموعة المتغيرات المضافة إلى مستند أو قالب. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | يحصل على أو يعين[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | يحصل على عدد إصدارات المستند التي تم تخزينها في مستند DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | يوفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | يتم استدعاؤها أثناء إجراءات معالجة المستندات المختلفة عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | يوفر الوصول إلى العلامة المائية للمستند. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | يعيد مجموعة تمثل قائمة من الوظائف الإضافية لجزء المهام. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | يوفر الوصول إلى خيارات حماية الكتابة في المستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | يقبل جميع التغييرات المتعقبة في المستند. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر لزيارة نهاية المستند. |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر لزيارة بداية المستند. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | يضيف العقدة المحددة إلى نهاية قائمة العقد الفرعية لهذه العقدة. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | يضيف المستند المحدد إلى نهاية هذا المستند. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | يضيف المستند المحدد إلى نهاية هذا المستند. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | ينظف الأنماط والقوائم غير المستخدمة من المستند. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | ينظف الأنماط والقوائم غير المستخدمة من المستند بناءً على ما تم تقديمه[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | يقوم بإجراء نسخة عميقة من`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | يقارن هذا المستند بمستند آخر وينتج تغييرات حسب عدد عمليات التحرير والتنسيق[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن هذا المستند بمستند آخر وينتج تغييرات نتيجة لعدد من عمليات التحرير والتنسيق[`Revision`](../revision/) . يسمح بتحديد خيارات المقارنة باستخدام[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | نسخ الأنماط من القالب المحدد إلى مستند. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | نسخ الأنماط من القالب المحدد إلى مستند. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | ينشئ متصفحًا يمكن استخدامه للتنقل بين العقد وقراءتها. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | إذا لم تحتوي الوثيقة على أي أقسام، فسيتم إنشاء قسم واحد يحتوي على فقرة واحدة. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | يحول التنسيق المحدد في أنماط الجدول إلى تنسيق مباشر على الجداول في المستند. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | يعيد`Document` كائن يمثل نطاقًا محددًا من الصفحات. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | يعيد عقدة فرعية رقم N تطابق النوع المحدد. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | يوفر الدعم لكل تكرار للأسلوب على العقد الفرعية لهذه العقدة. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | يحصل على حجم الصفحة والاتجاه ومعلومات أخرى حول الصفحة التي قد تكون مفيدة للطباعة أو العرض. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | استيراد عقدة من مستند آخر إلى المستند الحالي. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | استيراد عقدة من مستند آخر إلى المستند الحالي مع خيار التحكم في التنسيق. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | يقوم بإدراج العقدة المحددة مباشرة قبل عقدة المرجع المحددة. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | ينضم إلى التشغيلات بنفس التنسيق في جميع فقرات المستند. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | تغيير قيم نوع الحقل[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../aspose.words.fields/fieldstart/) ،[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ،[`FieldEnd`](../../aspose.words.fields/fieldend/) في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في رموز الحقول. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | يضيف العقدة المحددة إلى بداية قائمة العقد الفرعية لهذه العقدة. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Print](../../aspose.words/document/print/#print)() | يطبع المستند بأكمله على الطابعة الافتراضية. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم). |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | اطبع المستند بأكمله على الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم). |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم) واسم المستند. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | يحمي المستند من التغييرات دون تغيير كلمة المرور الموجودة أو تعيين كلمة مرور عشوائية. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | يحمي المستند من التغييرات ويحدد بشكل اختياري كلمة مرور للحماية. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | يزيل جميع العقد الفرعية للعقدة الحالية. |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | يزيل الصفحات الفارغة من المستند. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | يزيل العقدة الفرعية المحددة. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | يزيل مراجع مخطط XML الخارجية من هذه الوثيقة. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | يزيل جميع وحدات الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | يزيل الكل[`SmartTag`](../../aspose.words.markup/smarttag/) العقد المنحدرة من العقدة الحالية. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | يعرض صفحة مستند فيGraphics الكائن إلى مقياس محدد. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | يعرض صفحة مستند فيGraphics الكائن إلى حجم محدد. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | يحفظ المستند في ملف. يحدد تلقائيًا تنسيق الحفظ من الامتداد. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | يحفظ المستند في مجرى باستخدام التنسيق المحدد. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحفظ المستند في مجرى باستخدام خيارات الحفظ المحددة. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | يحفظ المستند في ملف بالتنسيق المحدد. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحفظ المستند في ملف باستخدام خيارات الحفظ المحددة. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يرسل المستند إلى متصفح العميل. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | يحدد قائمة العقد المطابقة لتعبير XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | يحدد الأول[`Node`](../node/) الذي يتطابق مع تعبير XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | يبدأ تلقائيًا بوضع علامة على جميع التغييرات الإضافية التي تقوم بها على المستند برمجيًا باعتبارها تغييرات مراجعة. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | يبدأ تلقائيًا بوضع علامة على جميع التغييرات الإضافية التي تقوم بها على المستند برمجيًا باعتبارها تغييرات مراجعة. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | يوقف وضع علامة تلقائية على تغييرات المستند باعتبارها مراجعات. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | إلغاء ربط الحقول في المستند بأكمله. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | يزيل الحماية من المستند بغض النظر عن كلمة المرور. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | يزيل الحماية من المستند إذا تم تحديد كلمة مرور صحيحة. |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | تحديث[`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/) خاصية جميع الحواشي السفلية والختامية في المستند. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | تحديث قيم الحقول في المستند بأكمله. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | تحديث تسميات القائمة لجميع عناصر القائمة في المستند. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | إعادة بناء تخطيط الصفحة للمستند. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | تحديثات [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) من المستند باستخدام الخيارات الافتراضية. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | تحديثات [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) من المستند وفقًا للخيارات المحددة. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | تحديث خصائص عدد الكلمات في المستند. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | تحديث خصائص عدد الكلمات في المستند، ويتم التحديث بشكل اختياري[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) الملكية. |

## ملاحظات

ال`Document` هو كائن مركزي في مكتبة Aspose.Words.

لتحميل مستند موجود في أي من[`LoadFormat`](../loadformat/) التنسيقات، مرر اسم الملف أو مجرى إلى أحد`Document` المنشئون. لإنشاء مستند فارغ، اتصل بالمنشئ بدون معلمات.

استخدم إحدى عمليات التحميل الزائد لطريقة الحفظ لحفظ المستند في أي من ملفات [`SaveFormat`](../saveformat/) التنسيقات.

لرسم صفحات المستند مباشرة على**الرسومات** كائن الاستخدام [`RenderToScale`](./rendertoscale/) أو[`RenderToSize`](./rendertosize/) طريقة.

لطباعة المستند، استخدم أحد[`Print`](./print/) طُرق.

[`MailMerge`](./mailmerge/)هو محرك إعداد التقارير الخاص بـ Aspose.Words الذي يسمح بملء التقارير المصممة في Microsoft Word بالبيانات من مصادر بيانات مختلفة بسرعة وسهولة. يمكن أن تكون البيانات من DataSet أو DataTable أو DataView أو IDataReader أو مجموعة من القيم.**دمج البريد** سيقوم بفحص السجلات الموجودة في مصدر البيانات وإدراجها في حقول دمج البريد في المستند وتنميتها حسب الضرورة.

`Document` يخزن معلومات على مستوى المستند مثل[`Styles`](../documentbase/styles/) ، [`BuiltInDocumentProperties`](./builtindocumentproperties/) ،[`CustomDocumentProperties`](./customdocumentproperties/) ، القوائم والماكرو. يمكن الوصول إلى معظم هذه الكائنات عبر الخصائص المقابلة لـ`Document`.

ال`Document` هي عقدة جذرية لشجرة تحتوي على جميع العقد الأخرى للمستند. الشجرة عبارة عن نمط تصميم مركب ومشابهة لـ XmlDocument في كثير من النواحي. يمكن معالجة محتوى المستند بحرية برمجيًا:

* يمكن الوصول إلى عقد المستند عبر المجموعات المكتوبة، على سبيل المثال[`Sections`](./sections/) ، [`ParagraphCollection`](../paragraphcollection/) إلخ.
* يمكن تحديد عقد المستند حسب نوع العقدة باستخدام [`GetChildNodes`](../compositenode/getchildnodes/) أو باستخدام استعلام XPath مع[`SelectNodes`](../compositenode/selectnodes/) أو[`SelectSingleNode`](../compositenode/selectsinglenode/).
* يمكن إضافة عقد المحتوى أو إزالتها من أي مكان في المستند باستخدام [`InsertBefore`](../compositenode/insertbefore/) ،[`InsertAfter`](../compositenode/insertafter/) ، [`RemoveChild`](../compositenode/removechild/) وطرق other التي توفرها الفئة الأساسية[`CompositeNode`](../compositenode/).
* يمكن تغيير سمات التنسيق لكل عقدة عبر خصائص تلك العقدة.

فكر في استخدام[`DocumentBuilder`](../documentbuilder/) وهذا يبسط مهمة إنشاء x000d_ برمجيًا أو ملء شجرة المستند.

ال`Document` يمكن أن تحتوي فقط[`Section`](../section/) أشياء.

في Microsoft Word، يجب أن يحتوي المستند الصحيح على قسم واحد على الأقل.

## أمثلة

يوضح كيفية تنفيذ دمج البريد باستخدام البيانات من جدول البيانات.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام جدول البيانات كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريدي واحد:
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
