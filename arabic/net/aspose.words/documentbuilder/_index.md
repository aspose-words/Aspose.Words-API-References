---
title: DocumentBuilder
second_title: Aspose.Words لمراجع .NET API
description: يوفر طرقًا لإدراج النص والصور والمحتويات الأخرى  وتحديد تنسيق الخط والفقرة والقسم.
type: docs
weight: 440
url: /ar/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

يوفر طرقًا لإدراج النص والصور والمحتويات الأخرى ، وتحديد تنسيق الخط والفقرة والقسم.

```csharp
public class DocumentBuilder
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DocumentBuilder](documentbuilder#constructor)() | تهيئة مثيل جديد لهذه الفئة. |
| [DocumentBuilder](documentbuilder#constructor_1)(Document) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold) { get; set; } | True إذا كان تنسيق الخط عريض . |
| [CellFormat](../../aspose.words/documentbuilder/cellformat) { get; } | إرجاع كائن يمثل خصائص تنسيق خلايا الجدول الحالية. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode) { get; } | يحصل على العقدة المحددة حاليًا في DocumentBuilder هذا. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph) { get; } | الحصول على الفقرة المحددة حاليًا في DocumentBuilder . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection) { get; } | يحصل على القسم المحدد حاليًا في DocumentBuilder هذا. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory) { get; } | الحصول على القصة المحددة حاليًا في DocumentBuilder هذا. |
| [Document](../../aspose.words/documentbuilder/document) { get; set; } | يحصل أو يحدد ملف[`Document`](./document) الكائن الذي يرتبط به هذا الكائن ._ x000d_ |
| [Font](../../aspose.words/documentbuilder/font) { get; } | إرجاع كائن يمثل خصائص تنسيق الخط الحالية. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph) { get; } | إرجاع صحيح إذا كان المؤشر في نهاية الفقرة الحالية. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph) { get; } | إرجاع صحيح إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر) ._ x000d_ |
| [Italic](../../aspose.words/documentbuilder/italic) { get; set; } | True إذا تم تنسيق الخط على أنه مائل. |
| [ListFormat](../../aspose.words/documentbuilder/listformat) { get; } | إرجاع كائن يمثل خصائص تنسيق القائمة الحالية. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup) { get; } | إرجاع كائن يمثل إعداد الصفحة الحالية وخصائص القسم. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat) { get; } | إرجاع كائن يمثل خصائص تنسيق الفقرة الحالية. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat) { get; } | إرجاع كائن يمثل خصائص تنسيق صف الجدول الحالي. |
| [Underline](../../aspose.words/documentbuilder/underline) { get; set; } | الحصول على / مجموعات نوع التسطير للخط الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow)(int, int) | حذف صف من الجدول . |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark)(string) | وضع علامة على الموضع الحالي في المستند كنهاية إشارة مرجعية. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark)(string) | تعليم الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع في خلية جدول. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange#endeditablerange)() | وضع علامة على الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange#endeditablerange_1)(EditableRangeStart) | وضع علامة على الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [EndRow](../../aspose.words/documentbuilder/endrow)() | إنهاء صف جدول في المستند. |
| [EndTable](../../aspose.words/documentbuilder/endtable)() | إنهاء جدول في المستند. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak)(BreakType) | إدراج فاصل من النوع المحدد في المستند. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell)() | إدراج خلية جدول في المستند. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart#insertchart_1)(ChartType, double, double) | إدراج كائن مخطط في المستند وقياسه إلى الحجم المحدد. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج كائن مخطط في المستند وقياسه إلى الحجم المحدد. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox#insertcheckbox_1)(string, bool, int) | يُدرج حقل نموذج خانة اختيار في الموضع الحالي. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox#insertcheckbox)(string, bool, bool, int) | يُدرج حقل نموذج خانة اختيار في الموضع الحالي. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox)(string, string[], int) | يتم إدراج حقل نموذج مربع تحرير وسرد في الموضع الحالي. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument#insertdocument)(Document, ImportFormatMode) | إدراج مستند في موضع المؤشر . |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | إدراج مستند في موضع المؤشر . |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield_1)(string) | إدراج حقل Word في مستند وتحديث نتيجة الحقل. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield)(FieldType, bool) | إدراج حقل Word في مستند وتحديث نتيجة الحقل اختياريًا. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield_2)(string, string) | إدراج حقل Word في مستند بدون تحديث نتيجة الحقل. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote#insertfootnote)(FootnoteType, string) | إدراج حاشية سفلية أو تعليق ختامي في المستند. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote#insertfootnote_1)(FootnoteType, string, string) | إدراج حاشية سفلية أو تعليق ختامي في المستند. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule)() | إدراج شكل قاعدة أفقية في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml)(string) | إدراج سلسلة HTML في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml_2)(string, bool) | إدراج سلسلة HTML في المستند. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml_1)(string, HtmlInsertOptions) | لإدراج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink)(string, string, bool) | إدراج ارتباط تشعبي في المستند. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage)(byte[]) | لإدراج صورة من مصفوفة بايت في المستند. تم إدراج الصورة في السطر وبمقياس 100٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_3)(Image) | لإدراج صورة من .NETImage في المستند. تم إدراج الصورة في السطر وبمقياس 100٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_6)(Stream) | لإدراج صورة من دفق في المستند. تم إدراج الصورة في السطر وبمقياس 100٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_9)(string) | يقوم بإدراج صورة من ملف أو عنوان URL في المستند. تم إدراج الصورة في السطر وبمقياس 100٪. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_2)(byte[], double, double) | إدراج صورة مضمنة من مصفوفة بايت في المستند وقياسها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_5)(Image, double, double) | إدراج صورة مضمنة من .NETImage في المستند وقياسه إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_8)(Stream, double, double) | إدراج صورة مضمنة من دفق في المستند وقياسها إلى الحجم المحدد ._ x000d_ |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_11)(string, double, double) | إدراج صورة مضمنة من ملف أو عنوان URL في المستند وقياسها إلى الحجم المحدد. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج صورة من مصفوفة بايت في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | لإدراج صورة من .NETImage كائن في الموضع والحجم المحددين ._ x000d_ |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | لإدراج صورة من تيار في الموضع والحجم المحددين. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode)(Node) | إدراج عقدة على مستوى النص داخل الفقرة الحالية قبل المؤشر. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject)(Stream, string, bool, Stream) | إدراج كائن OLE مضمن من دفق إلى المستند. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject_1)(string, bool, bool, Stream) | إدراج عنصر OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject_2)(string, string, bool, bool, Stream) | إدراج عنصر OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام معلمة progID معينة. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon)(Stream, string, string, string) | إدراج كائن OLE مضمن كرمز من تدفق إلى المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID معينة. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon_1)(string, bool, string, string) | إدراج كائن OLE مضمن أو مرتبط كرمز في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon_2)(string, string, bool, string, string) | إدراج كائن OLE مضمن أو مرتبط كرمز في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID معينة. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_1)(string, double, double) | إدراج كائن فيديو عبر الإنترنت في المستند وقياسه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_3)(string, string, byte[], double, double) | إدراج كائن فيديو عبر الإنترنت في المستند وقياسه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج كائن فيديو عبر الإنترنت في المستند وقياسه إلى الحجم المحدد. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج كائن فيديو عبر الإنترنت في المستند وقياسه إلى الحجم المحدد. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph)() | إدراج فاصل فقرة في المستند. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape#insertshape_1)(ShapeType, double, double) | إدراج شكل مضمّن بنوع وحجم محددين. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | إدراج شكل عائم مع موضع وحجم ونوع التفاف النص المحدد. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline#insertsignatureline)(SignatureLineOptions) | إدراج سطر توقيع في الموضع الحالي . |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | إدراج سطر توقيع في الموضع المحدد. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator)() | إدراج فاصل الأنماط في المستند. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents)(string) | يقوم بإدراج حقل TOC (جدول المحتويات) في المستند. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput)(string, TextFormFieldType, string, string, int) | يُدرج حقل نموذج نصي في الموضع الحالي. |
| [MoveTo](../../aspose.words/documentbuilder/moveto)(Node) | لنقل المؤشر إلى عقدة سطرية أو إلى نهاية فقرة. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark#movetobookmark)(string) | ينقل المؤشر إلى إشارة مرجعية . |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark#movetobookmark_1)(string, bool, bool) | ينقل المؤشر إلى إشارة مرجعية بدقة أكبر ._ x000d_ |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell)(int, int, int, int) | ينقل المؤشر إلى خلية جدول في القسم الحالي. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend)() | ينقل المؤشر إلى نهاية المستند. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart)() | ينقل المؤشر إلى بداية المستند. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield)(Field, bool) | ينقل المؤشر إلى حقل في المستند. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter)(HeaderFooterType) | نقل المؤشر إلى بداية رأس أو تذييل في القسم الحالي. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield#movetomergefield)(string) | ينقل المؤشر إلى موضع خارج حقل الدمج المحدد ويزيل حقل الدمج. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield#movetomergefield_1)(string, bool, bool) | نقل حقل الدمج إلى حقل الدمج المحدد. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph)(int, int) | تحريك المؤشر إلى فقرة في القسم الحالي. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection)(int) | ينقل المؤشر إلى بداية النص في قسم محدد. |
| [PopFont](../../aspose.words/documentbuilder/popfont)() | استرداد تنسيق الأحرف المحفوظة مسبقًا في المكدس. |
| [PushFont](../../aspose.words/documentbuilder/pushfont)() | يحفظ تنسيق الأحرف الحالي في المكدس. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark)(string) | وضع علامة على الموضع الحالي في المستند كبداية إشارة مرجعية. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark)(string) | تعليم الموضع الحالي في المستند كبداية إشارة عمود. يجب أن يكون الموضع في خلية جدول. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange)() | وضع علامة على الموضع الحالي في المستند كبداية لنطاق قابل للتحرير. |
| [StartTable](../../aspose.words/documentbuilder/starttable)() | يبدأ جدول في المستند . |
| [Write](../../aspose.words/documentbuilder/write)(string) | لإدراج سلسلة في المستند في موضع الإدخال الحالي. |
| [Writeln](../../aspose.words/documentbuilder/writeln#writeln)() | إدراج فاصل فقرة في المستند. |
| [Writeln](../../aspose.words/documentbuilder/writeln#writeln_1)(string) | إدراج سلسلة وفاصل فقرة في المستند. |

### ملاحظات

**DocumentBuilder** يجعل عملية بناء أ **وثيقة** أسهل. **وثيقة**هو كائن مركب يتكون من شجرة من العقد وأثناء إدخال content العقد مباشرة في الشجرة ، فإنه يتطلب فهمًا جيدًا لهيكل الشجرة. **DocumentBuilder** هي "واجهة" للهيكل المعقد لـ **وثيقة** ويسمح بإدراج المحتوى والتنسيق بسرعة وسهولة.

إنشاء **DocumentBuilder** وربطها بـ[`Document`](./document).

ال **DocumentBuilder** يحتوي على مؤشر داخلي حيث سيتم إدراج النص عند الاتصال[`Write`](./write) و[`Writeln`](./writeln) و[`InsertBreak`](./insertbreak) وطرق أخرى. يمكنك التنقل في ملف **DocumentBuilder** قم بالمؤشر إلى موقع مختلف في مستند باستخدام طرق MoveToXXX المختلفة.

استخدم ال[`Font`](./font) لتحديد تنسيق الأحرف الذي سيتم تطبيقه على كل النص المدرج من الموضع الحالي في المستند فصاعدًا.

استخدم ال[`ParagraphFormat`](./paragraphformat) الخاصية لتحديد تنسيق الفقرة لـ current وجميع الفقرات التي سيتم إدراجها.

استخدم ال[`PageSetup`](./pagesetup)لتحديد خصائص الصفحة والقسم للقسم current وجميع الأقسام التي سيتم إدراجها.

استخدم ال[`CellFormat`](./cellformat) و[`RowFormat`](./rowformat) خصائص تحديد x000d_ خصائص التنسيق لخلايا الجدول والصفوف. استخدم ملف[`InsertCell`](./insertcell) و_ x000d_[`EndRow`](./endrow) طرق لبناء الجدول.

لاحظ أن **الخط** و **تنسيق الفقرة** و **اعداد الصفحة** يتم تحديث الخصائص عندما تنتقل إلى مكان مختلف في المستند لتعكس خصائص التنسيق المتوفرة في الموقع الجديد.

### أمثلة

يوضح كيفية استخدام منشئ المستندات لإنشاء جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ابدأ الجدول ، ثم املأ الصف الأول بخليتين.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// اتصل بطريقة "EndRow" الخاصة بالباني لبدء صف جديد.
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

// حدد أننا نريد رؤوس وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// أنشئ الرؤوس ، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع رأس.
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

// تعيين خيارات تنسيق الجدول لمنشئ المستندات
// سيطبقها على كل صف وخلية نضيفها معها.
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

// سيؤدي تغيير التنسيق إلى تطبيقه على الخلية الحالية ،
// وأي خلايا جديدة ننشئها باستخدام المنشئ بعد ذلك.
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

* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
