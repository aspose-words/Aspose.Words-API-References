---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.DocumentBuilder—الحل الخاص بك لإدراج النصوص والصور وعناصر التنسيق في المستندات بسهولة.
type: docs
weight: 660
url: /ar/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

يوفر طرقًا لإدراج النصوص والصور والمحتوى الآخر، وتحديد تنسيق الخط والفقرة والقسم.

لمعرفة المزيد، قم بزيارة[نظرة عامة على منشئ المستندات](https://docs.aspose.com/words/net/document-builder-overview/) مقالة توثيقية.

```csharp
public class DocumentBuilder
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | يقوم بتهيئة مثيل جديد لهذه الفئة. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه غامق. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | يعيد كائنًا يمثل خصائص تنسيق خلايا الجدول الحالية. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | يحصل على العقدة المحددة حاليًا في DocumentBuilder هذا. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | يحصل على الفقرة المحددة حاليًا في هذه`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | يحصل على القسم المحدد حاليًا في هذا`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | يحصل على القصة المحددة حاليًا في هذه`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | يحصل على علامة المستند المنظمة المحددة حاليًا في هذا`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | يحصل على أو يعين[`Document`](./document/) الكائن الذي يرتبط به هذا الكائن. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | يعيد كائنًا يمثل خصائص تنسيق الخط الحالية. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | إرجاع`حقيقي` إذا كان المؤشر في نهاية الفقرة الحالية. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | إرجاع**حقيقي** إذا كان المؤشر في نهاية علامة مستند منظم. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | إرجاع`حقيقي`إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه مائل. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | يعيد كائنًا يمثل خصائص تنسيق القائمة الحالية. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | يعيد كائنًا يمثل إعداد الصفحة الحالية وخصائص القسم. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | يعيد كائنًا يمثل خصائص تنسيق الفقرة الحالية. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | يعيد كائنًا يمثل خصائص تنسيق صف الجدول الحالي. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | يحصل على/يحدد نوع التسطير للخط الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | يحذف صفًا من جدول. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | يُحدِّد الموضع الحالي في المستند كعلامة مرجعية لنهاية العمود. يجب أن يكون الموضع في خلية جدول. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | يحدد الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | يحدد الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | ينهي صف جدول في المستند. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | ينهي جدولًا في المستند. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | يقوم بإدراج فاصل من النوع المحدد في المستند. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | إدراج خلية جدول في المستند. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | يقوم بإدراج كائن مخطط في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | يقوم بإدراج كائن مخطط في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج كائن مخطط في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | يقوم بإدراج كائن مخطط في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | يقوم بإدراج حقل نموذج مربع الاختيار في الموضع الحالي. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | يقوم بإدراج حقل نموذج مربع الاختيار في الموضع الحالي. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | يقوم بإدراج حقل نموذج المجموعة في الموضع الحالي. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | إدراج مستند في موضع المؤشر. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | إدراج مستند في موضع المؤشر. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | يقوم بإدراج مستند مضمن في موضع المؤشر. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | يقوم بإدراج حقل Word في مستند ويقوم بتحديث نتيجة الحقل. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | يقوم بإدراج حقل Word في مستند ويقوم بشكل اختياري بتحديث نتيجة الحقل. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | يقوم بإدراج حقل Word في مستند دون تحديث نتيجة الحقل. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | يقوم بإدراج حاشية سفلية أو تعليق ختامي في المستند. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | يقوم بإدراج حاشية سفلية أو تعليق ختامي في المستند. |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | إدراجات[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/) الكائن في الموضع الحالي. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | تجميع الأشكال التي تم تمريرها كمعلمة في عقدة GroupShape جديدة يتم إدراجها في الموضع الحالي. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | تجميع الأشكال التي تم تمريرها كمعلمة في عقدة GroupShape جديدة بالحجم المحدد والتي يتم إدراجها في الموضع المحدد. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | يقوم بإدراج شكل مسطرة أفقية في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | يقوم بإدراج سلسلة HTML في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | يقوم بإدراج سلسلة HTML في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | يُدرج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | إدراج ارتباط تشعبي في المستند. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | يُدرج صورة من مصفوفة بايتات في المستند. تُدرج الصورة مضمنةً وبمقياس ١٠٠٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | إدراج صورة من .NETImage كائن في المستند. الصورة مُدرجة ضمنيًا وبمقياس ١٠٠٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | يُدرج صورة من تدفق في المستند. تُدرج الصورة مضمنةً وبمقياس ١٠٠٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | يُدرج صورة من ملف أو رابط في المستند. تُدرج الصورة مضمنةً وبمقياس ١٠٠٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | يقوم بإدراج صورة مضمنة من مجموعة بايتات في المستند ويقوم بتغيير حجمها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | يقوم بإدراج صورة مضمنة من .NETImage الكائن في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | يقوم بإدراج صورة مضمنة من مجرى في المستند ويقوم بتغيير حجمها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | يقوم بإدراج صورة مضمنة من ملف أو عنوان URL في المستند ويقوم بتغيير حجمها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج صورة من مجموعة بايتات في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | إدراج صورة من .NETImage الكائن في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج صورة من مجرى في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | يقوم بإدراج عقدة قبل المؤشر. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | يقوم بإدراج كائن OLE مضمن من مجرى إلى المستند. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | يُدرج كائن OLE مُضمّنًا أو مُرتبطًا من ملف إلى المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | يُدرج كائن OLE مُضمّنًا أو مُرتبطًا من ملف إلى المستند. يكتشف نوع كائن OLE باستخدام مُعامل progID المُعطى. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | يُدرج كائن OLE مُضمّن كأيقونة من دفق إلى المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام مُعامل progID المُعطى. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | يُدرج كائن OLE مُضمّنًا أو مُرتبطًا كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | يُدرج كائن OLE مُضمّنًا أو مُرتبطًا كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام مُعامل progID المُحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | يقوم بإدراج فاصل فقرة في المستند. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | إدراج شكل مضمن بنوع وحجم محددين. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | إدراج شكل عائم حر مع موضع وحجم ونوع التفاف النص المحدد. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | يقوم بإدراج سطر توقيع في الموضع الحالي. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | يقوم بإدراج سطر توقيع في الموضع المحدد. |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | يُدرج[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) في المستند. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | إدراج فاصل النمط في المستند. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | يقوم بإدراج حقل TOC (جدول المحتويات) في المستند. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | يقوم بإدراج حقل نموذج نصي في الموضع الحالي. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | يحرك المؤشر إلى عقدة مضمنة أو إلى نهاية فقرة. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | يحرك المؤشر إلى الإشارة المرجعية. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | يحرك المؤشر إلى إشارة مرجعية بدقة أكبر. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | يحرك المؤشر إلى خلية الجدول في القسم الحالي. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | يحرك المؤشر إلى نهاية المستند. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | يحرك المؤشر إلى بداية المستند. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | يحرك المؤشر إلى حقل في المستند. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | يحرك المؤشر إلى بداية الرأس أو التذييل في القسم الحالي. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | يحرك المؤشر إلى موضع يقع خلف حقل الدمج المحدد ويزيل حقل الدمج. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | ينقل حقل الدمج إلى حقل الدمج المحدد. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | يحرك المؤشر إلى فقرة في القسم الحالي. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | يحرك المؤشر إلى بداية النص في قسم محدد. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | يحرك المؤشر إلى علامة مستند منظمة في القسم الحالي. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | يحرك المؤشر إلى علامة المستند المنظم. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | يسترجع تنسيق الأحرف المحفوظ مسبقًا على المكدس. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | يحفظ تنسيق الأحرف الحالي على المكدس. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | يحدد الموضع الحالي في المستند كبداية للإشارة المرجعية. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | يُحدد الموضع الحالي في المستند كبداية إشارة مرجعية للعمود. يجب أن يكون الموضع في خلية جدول. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | يبدأ جدولًا في المستند. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | يقوم بإدراج سلسلة في المستند في موضع الإدراج الحالي. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | يقوم بإدراج فاصل فقرة في المستند. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | يقوم بإدراج سلسلة وفاصل فقرة في المستند. |

## ملاحظات

`DocumentBuilder` يجعل عملية البناء[`Document`](../document/) أسهل. [`Document`](../document/) هو كائن مركب يتكون من شجرة من العقد، وعلى الرغم من إمكانية إدراج عقد content مباشرة في الشجرة، إلا أن ذلك يتطلب فهمًا جيدًا لبنية الشجرة. `DocumentBuilder` "إنها واجهة" للهيكل المعقد لـ[`Document`](../document/) ويسمح بإدراج المحتوى والتنسيق بسرعة وسهولة.

إنشاء`DocumentBuilder` وربطها بـ[`Document`](../document/).

ال`DocumentBuilder` يحتوي على مؤشر داخلي حيث سيتم إدراج النص عند الاتصال[`Write`](./write/) ،[`Writeln`](./writeln/) ،[`InsertBreak`](./insertbreak/) وطرق أخرى. يمكنك التنقل عبر`DocumentBuilder` قم بتوجيه المؤشر إلى موقع مختلف في مستند باستخدام طرق MoveToXXX المختلفة.

استخدم[`Font`](./font/) الخاصية لتحديد تنسيق الأحرف الذي سيتم تطبيقه على كل النص المدرج من الموضع الحالي في المستند فصاعدًا.

استخدم[`ParagraphFormat`](./paragraphformat/) الخاصية لتحديد تنسيق الفقرة لـ current وجميع الفقرات التي سيتم إدراجها.

استخدم[`PageSetup`](./pagesetup/) الخاصية لتحديد خصائص الصفحة والقسم للقسم الحالي وجميع الأقسام التي سيتم إدراجها.

استخدم[`CellFormat`](./cellformat/) و[`RowFormat`](./rowformat/) خصائص لتحديد خصائص تنسيق x000d_ لخلايا وصفوف الجدول. استخدم[`InsertCell`](./insertcell/) و [`EndRow`](./endrow/) طرق بناء الجدول.

لاحظ أن[`Font`](./font/) ،[`ParagraphFormat`](./paragraphformat/) و[`PageSetup`](./pagesetup/) يتم تحديث الخصائص كلما قمت بالانتقال إلى مكان مختلف في المستند لتعكس خصائص التنسيق المتوفرة في الموقع الجديد.

## أمثلة

يوضح كيفية استخدام منشئ المستندات لإنشاء جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ابدأ الجدول، ثم املأ الصف الأول بخليتين.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

//استدعاء طريقة "EndRow" الخاصة بالمنشئ لبدء صف جديد.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// قم بإنشاء الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من أنواع الرؤوس.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

يوضح كيفية إنشاء جدول بحدود مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

//إعداد خيارات تنسيق الجدول لمنشئ المستندات
// سيتم تطبيقها على كل صف وخلية نضيفها معها.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// سيؤدي تغيير التنسيق إلى تطبيقه على الخلية الحالية،
//وأي خلايا جديدة نقوم بإنشائها باستخدام المنشئ بعد ذلك.
// لن يؤثر هذا على الخلايا التي أضفناها مسبقًا.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// زيادة ارتفاع الصف ليتناسب مع النص الرأسي.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
