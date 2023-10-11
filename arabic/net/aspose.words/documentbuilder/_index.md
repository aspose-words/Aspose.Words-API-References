---
title: Class DocumentBuilder
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.DocumentBuilder فصل. يوفر طرقًا لإدراج النصوص والصور والمحتويات الأخرى وتحديد تنسيق الخط والفقرة والأقسام.
type: docs
weight: 450
url: /ar/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

يوفر طرقًا لإدراج النصوص والصور والمحتويات الأخرى، وتحديد تنسيق الخط والفقرة والأقسام.

لمعرفة المزيد، قم بزيارة[نظرة عامة على منشئ المستندات](https://docs.aspose.com/words/net/document-builder-overview/) مقالة توثيقية.

```csharp
public class DocumentBuilder
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | تهيئة مثيل جديد لهذه الفئة. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | صحيح إذا كان الخط منسقًا بالخط الغامق. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | إرجاع كائن يمثل خصائص تنسيق خلايا الجدول الحالي. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | يحصل على العقدة المحددة حاليًا في DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | يحصل على الفقرة المحددة حاليًا في هذا`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | يحصل على القسم المحدد حاليًا في هذا`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | يحصل على القصة المحددة حاليًا في هذا`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | يحصل على علامة المستند المنظمة المحددة حاليًا في هذا`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | الحصول على أو تعيين[`Document`](./document/)الكائن الذي يرتبط به هذا الكائن. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | إرجاع كائن يمثل خصائص تنسيق الخط الحالية. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | إرجاع`حقيقي` إذا كان المؤشر في نهاية الفقرة الحالية. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | إرجاع **حقيقي** إذا كان المؤشر في نهاية علامة مستند منظم. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | إرجاع`حقيقي` إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | صحيح إذا كان الخط منسقًا بالخط المائل. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | إرجاع كائن يمثل خصائص تنسيق القائمة الحالية. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | إرجاع كائن يمثل إعداد الصفحة الحالية وخصائص القسم. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | إرجاع كائن يمثل خصائص تنسيق الفقرة الحالية. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | إرجاع كائن يمثل خصائص تنسيق صف الجدول الحالي. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | يحصل على/يحدد نوع التسطير للخط الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | حذف صف من الجدول. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع في خلية الجدول. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | يحدد الموضع الحالي في المستند كنهاية نطاق قابلة للتحرير. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | يحدد الموضع الحالي في المستند كنهاية نطاق قابلة للتحرير. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | إنهاء صف الجدول في المستند. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | إنهاء جدول في المستند. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | إدراج فاصل من النوع المحدد في المستند. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | إدراج خلية جدول في المستند. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | إدراج كائن مخطط في المستند وتغيير حجمه إلى الحجم المحدد. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج كائن مخطط في المستند وتغيير حجمه إلى الحجم المحدد. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | إدراج حقل نموذج خانة الاختيار في الموضع الحالي. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | إدراج حقل نموذج خانة الاختيار في الموضع الحالي. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | إدراج حقل نموذج combobox في الموضع الحالي. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | إدراج مستند في موضع المؤشر. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | إدراج مستند في موضع المؤشر. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | إدراج حقل Word في المستند وتحديث نتيجة الحقل. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | يقوم بإدراج حقل Word في مستند ويقوم بتحديث نتيجة الحقل بشكل اختياري. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | إدراج حقل Word في مستند دون تحديث نتيجة الحقل. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | إدراج حاشية سفلية أو تعليق ختامي في المستند. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | إدراج حاشية سفلية أو تعليق ختامي في المستند. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | إدراج شكل مسطرة أفقية في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | إدراج سلسلة HTML في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | إدراج سلسلة HTML في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | يقوم بإدراج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | إدراج ارتباط تشعبي في المستند. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | إدراج صورة من مصفوفة بايت في المستند. تم إدراج الصورة سطريًا وبحجم 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | إدراج صورة من .NETImage كائن في المستند. تم إدراج الصورة سطريًا وبحجم 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | يقوم بإدراج صورة من الدفق إلى المستند. تم إدراج الصورة سطريًا وبحجم 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | إدراج صورة من ملف أو عنوان URL في المستند. تم إدراج الصورة سطريًا وبحجم 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | إدراج صورة مضمّنة من مصفوفة بايت في المستند وتغيير حجمها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | إدراج صورة مضمنة من .NETImage كائن في المستند وقياسه إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | إدراج صورة مضمّنة من الدفق في المستند وتغيير حجمها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | إدراج صورة مضمنة من ملف أو عنوان URL في المستند وتغيير حجمها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج صورة من مصفوفة بايت في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج صورة من .NETImageكائن في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج صورة من دفق في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | إدراج عقدة قبل المؤشر. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | إدراج كائن OLE مضمن من دفق في المستند. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | يقوم بإدراج كائن OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | يقوم بإدراج كائن OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام معلمة progID المحددة. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | إدراج كائن OLE مضمن كأيقونة من دفق في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID المحددة. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | يقوم بإدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | يقوم بإدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID المحددة. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | إدراج فاصل فقرة في المستند. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | إدراج شكل سطري بالنوع والحجم المحددين. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج شكل عائم بموضع وحجم ونوع التفاف النص المحدد. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | إدراج سطر التوقيع في الموضع الحالي. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | إدراج سطر التوقيع في الموضع المحدد. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | إدراج فاصل النمط في المستند. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | إدراج حقل TOC (جدول المحتويات) في المستند. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | إدراج حقل نموذج نصي في الموضع الحالي. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | ينقل المؤشر إلى إشارة مرجعية. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | ينقل المؤشر إلى إشارة مرجعية بدقة أكبر. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | ينقل المؤشر إلى خلية الجدول في القسم الحالي. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | يحرك المؤشر إلى نهاية المستند. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | ينقل المؤشر إلى بداية المستند. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | يحرك المؤشر إلى حقل في المستند. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | ينقل المؤشر إلى بداية الرأس أو التذييل في القسم الحالي. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | يحرك المؤشر إلى موضع يقع خارج حقل الدمج المحدد مباشرة ويزيل حقل الدمج. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | ينقل حقل الدمج إلى حقل الدمج المحدد. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | ينقل المؤشر إلى فقرة في القسم الحالي. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | ينقل المؤشر إلى بداية النص في قسم محدد. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | ينقل المؤشر إلى علامة مستند منظمة في القسم الحالي. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | يحرك المؤشر إلى علامة الوثيقة المنظمة. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | استرداد تنسيق الأحرف الذي تم حفظه مسبقًا على المكدس. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | يحفظ تنسيق الأحرف الحالي في المكدس. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | يحدد الموضع الحالي في المستند كبداية إشارة مرجعية. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | يحدد الموضع الحالي في المستند كبداية عمود الإشارة المرجعية. يجب أن يكون الموضع في خلية الجدول. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | يبدأ جدول في المستند. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | إدراج سلسلة في المستند في موضع الإدراج الحالي. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | إدراج فاصل فقرة في المستند. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | إدراج سلسلة وفاصل فقرة في المستند. |

### ملاحظات

`DocumentBuilder` يجعل عملية بناء أ[`Document`](../document/) أسهل. [`Document`](../document/) هو كائن مركب يتكون من شجرة من العقد، وبينما يكون من الممكن إدراج عقد content مباشرة في الشجرة، إلا أنه يتطلب فهمًا جيدًا لبنية الشجرة. `DocumentBuilder` هي "واجهة" للبنية المعقدة لـ[`Document`](../document/) ويسمح بإدراج المحتوى والتنسيق بسرعة وسهولة.

إنشاء`DocumentBuilder` وربطها بـ أ[`Document`](../document/).

ال`DocumentBuilder` يحتوي على مؤشر داخلي حيث سيتم إدراج النص عند الاتصال[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) وطرق أخرى. يمكنك التنقل في`DocumentBuilder` المؤشر إلى location مختلف في مستند باستخدام طرق MoveToXXX المتنوعة.

استخدم ال[`Font`](./font/)الخاصية لتحديد تنسيق الأحرف الذي سيتم تطبيقه على كل النص المدرج من الموضع الحالي في المستند فصاعدًا.

استخدم ال[`ParagraphFormat`](./paragraphformat/) الخاصية لتحديد تنسيق الفقرة لـ current وجميع الفقرات التي سيتم إدراجها.

استخدم ال[`PageSetup`](./pagesetup/) الخاصية لتحديد خصائص الصفحة والقسم للقسم current وكل الأقسام التي سيتم إدراجها.

استخدم ال[`CellFormat`](./cellformat/) و[`RowFormat`](./rowformat/) خصائص لتحديد خصائص التنسيق لخلايا وصفوف الجدول. المستخدم[`InsertCell`](./insertcell/) و [`EndRow`](./endrow/) طرق بناء الجدول.

لاحظ أن[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) و[`PageSetup`](./pagesetup/) يتم تحديث الخصائص كلما تنتقل إلى مكان مختلف في المستند لتعكس خصائص التنسيق المتوفرة في الموقع الجديد.

### أمثلة

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

// اتصل بطريقة "EndRow" الخاصة بالمنشئ لبدء صف جديد.
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

// أنشئ الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع رأس.
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

// ضبط خيارات تنسيق الجدول لمنشئ المستندات
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
// وأي خلايا جديدة نقوم بإنشائها مع المُنشئ بعد ذلك.
// لن يؤثر هذا على الخلايا التي أضفناها سابقًا.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// زيادة ارتفاع الصف ليناسب النص الرأسي.
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


