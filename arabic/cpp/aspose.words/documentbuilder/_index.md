---
title: "Aspose::Words::DocumentBuilder class"
linktitle: "DocumentBuilder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder class. يوفر طرقًا لإدراج النصوص، الصور وغيرها من المحتوى، وتحديد تنسيق الخط، الفقرة والقسم. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


يوفر طرقًا لإدراج النصوص، الصور ومحتويات أخرى، وتحديد تنسيق الخط، الفقرة والقسم. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/).

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | يحذف صفًا من جدول. |
| [DocumentBuilder](./documentbuilder/)() | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [EndBookmark](./endbookmark/)(const System::String\&) | يُعلِّم الموضع الحالي في المستند كنهاية إشارة مرجعية. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | يُعلِّم الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع داخل خلية جدول. |
| [EndEditableRange](./endeditablerange/)() | يُعلِّم الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | يُعلِّم الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [EndRow](./endrow/)() | ينهي صف جدول في المستند. |
| [EndTable](./endtable/)() | ينهي جدولًا في المستند. |
| [get_Bold](./get_bold/)() | صحيح إذا كان الخط مُنسقًا كغامق. |
| [get_CellFormat](./get_cellformat/)() | يرجع كائنًا يمثل خصائص تنسيق خلية الجدول الحالية. |
| [get_CurrentNode](./get_currentnode/)() | يحصل على العقدة المحددة حاليًا في هذا [DocumentBuilder](./). |
| [get_CurrentParagraph](./get_currentparagraph/)() | يحصل على الفقرة المحددة حاليًا في هذا [DocumentBuilder](./). |
| [get_CurrentSection](./get_currentsection/)() | يحصل على القسم المحدد حاليًا في هذا [DocumentBuilder](./). |
| [get_CurrentStory](./get_currentstory/)() | يحصل على القصة المحددة حاليًا في هذا [DocumentBuilder](./). |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | يحصل على علامة المستند المُنظمة المحددة حاليًا في هذا [DocumentBuilder](./). |
| [get_Document](./get_document/)() const | يحصل أو يعيّن كائن [Document](./get_document/) الذي تم إرفاق هذا الكائن به. |
| [get_Font](./get_font/)() | يرجع كائنًا يمثل خصائص تنسيق الخط الحالية. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | يرجع **true** إذا كان المؤشر في نهاية الفقرة الحالية. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | يرجع **true** إذا كان المؤشر في نهاية علامة مستند منسق. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | يرجع **true** إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر). |
| [get_Italic](./get_italic/)() | صحيح إذا كان الخط منسقًا كإيطالي. |
| [get_ListFormat](./get_listformat/)() | يرجع كائنًا يمثل خصائص تنسيق القائمة الحالية. |
| [get_PageSetup](./get_pagesetup/)() | يرجع كائنًا يمثل إعدادات الصفحة الحالية وخصائص القسم. |
| [get_ParagraphFormat](./get_paragraphformat/)() | يرجع كائنًا يمثل خصائص تنسيق الفقرة الحالية. |
| [get_RowFormat](./get_rowformat/)() | يرجع كائنًا يمثل خصائص تنسيق صف الجدول الحالي. |
| [get_Underline](./get_underline/)() | يحصل/يضبط نوع التسطير للخط الحالي. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | يدرج فاصلًا من النوع المحدد في المستند. |
| [InsertCell](./insertcell/)() | يدرج خلية جدول في المستند. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | يدرج حقل نموذج خانة اختيار في الموضع الحالي. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | يدرج حقل نموذج خانة اختيار في الموضع الحالي. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | يدرج حقل نموذج صندوق قائمة منسدلة في الموضع الحالي. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | يدرج مستندًا في موضع المؤشر. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يدرج مستندًا في موضع المؤشر. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يدرج مستندًا مضمنًا في موضع المؤشر. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | يدرج حقل Word في مستند ويحدّث نتيجة الحقل اختياريًا. |
| [InsertField](./insertfield/)(const System::String\&) | يدرج حقل Word في مستند ويحدّث نتيجة الحقل. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | يدرج حقل Word في مستند دون تحديث نتيجة الحقل. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | يدرج حاشية سفلية أو حاشية نهائية في المستند. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | يدرج حاشية سفلية أو حاشية نهائية في المستند. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | يدرج كائن [Forms2OleControl](../) في الموضع الحالي. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | يجمع الأشكال الممررة كمعامل في عقدة GroupShape جديدة تُدرج في الموضع الحالي. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | يجمع الأشكال الممررة كمعامل في عقدة GroupShape جديدة بالحجم المحدد تُدرج في الموضع المحدد. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | يدرج شكل قاعدة أفقية في المستند. |
| [InsertHtml](./inserthtml/)(const System::String\&) | يدرج سلسلة HTML في المستند. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | يدرج سلسلة HTML في المستند. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | يقوم بإدراج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | يقوم بإدراج ارتباط تشعبي في المستند. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | يقوم بإدراج صورة من كائن **Image** في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪. |
| [InsertImage](./insertimage/)(const System::String\&) | يقوم بإدراج صورة من ملف أو عنوان URL في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بإدراج صورة من تدفق بيانات في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | يقوم بإدراج صورة من مصفوفة بايتات في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | يقوم بإدراج صورة داخلية من كائن **Image** في المستند ويقوم بتحجيمها إلى الحجم المحدد. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | يقوم بإدراج صورة داخلية من ملف أو عنوان URL في المستند ويقوم بتحجيمها إلى الحجم المحدد. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | يقوم بإدراج صورة داخلية من تدفق بيانات في المستند ويقوم بتحجيمها إلى الحجم المحدد. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | يقوم بإدراج صورة داخلية من مصفوفة بايتات في المستند ويقوم بتحجيمها إلى الحجم المحدد. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج صورة من كائن **Image** في الموضع والحجم المحددين. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج صورة من تدفق بيانات في الموضع والحجم المحددين. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج صورة من مصفوفة بايتات في الموضع والحجم المحددين. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يقوم بإدراج عقدة قبل المؤشر. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بإدراج كائن OLE مدمج من تدفق بيانات في المستند. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بإدراج كائن OLE مدمج أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بإدراج كائن OLE مدمج أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام معامل progID المقدم. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | يقوم بإدراج كائن OLE مدمج أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتعليق. يكتشف نوع كائن OLE باستخدام امتداد الملف. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | يقوم بإدراج كائن OLE مدمج أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتعليق. يكتشف نوع كائن OLE باستخدام معامل progID المقدم. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | يقوم بإدراج كائن OLE مدمج كأيقونة من تدفق بيانات في المستند. يسمح بتحديد ملف الأيقونة والتعليق. يكتشف نوع كائن OLE باستخدام معامل progID المقدم. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد. |
| [InsertParagraph](./insertparagraph/)() | يقوم بإدراج فاصل فقرة في المستند. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | يقوم بإدراج شكل داخل السطر بالنوع والحجم المحددين. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | يقوم بإدراج شكل عائم بحرية بالموقع والحجم ونوع التفاف النص المحددين. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | يدرج سطر توقيع في الموضع الحالي. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | يدرج سطر توقيع في الموضع المحدد. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | يدرج [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) في المستند. |
| [InsertStyleSeparator](./insertstyleseparator/)() | يدرج فاصل نمط في المستند. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | يدرج حقل فهرس (table of contents) في المستند. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | يدرج حقل نموذج نصي في الموضع الحالي. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | ينقل المؤشر إلى إشارة مرجعية. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | ينقل المؤشر إلى إشارة مرجعية بدقة أكبر. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | ينقل المؤشر إلى خلية جدول في القسم الحالي. |
| [MoveToDocumentEnd](./movetodocumentend/)() | ينقل المؤشر إلى نهاية المستند. |
| [MoveToDocumentStart](./movetodocumentstart/)() | ينقل المؤشر إلى بداية المستند. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | ينقل المؤشر إلى حقل في المستند. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | ينقل المؤشر إلى بداية رأس أو تذييل في القسم الحالي. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | ينقل المؤشر إلى موضع يقع مباشرة بعد حقل الدمج المحدد ويزيل حقل الدمج. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | ينقل حقل الدمج إلى حقل الدمج المحدد. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | ينقل المؤشر إلى فقرة في القسم الحالي. |
| [MoveToSection](./movetosection/)(int32_t) | ينقل المؤشر إلى بداية النص في قسم محدد. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | ينقل المؤشر إلى علامة مستند منظم في القسم الحالي. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | ينقل المؤشر إلى علامة المستند المنظم. |
| [PopFont](./popfont/)() | يسترجع تنسيق الأحرف الذي تم حفظه مسبقًا على المكدس. |
| [PushFont](./pushfont/)() | يحفظ تنسيق الأحرف الحالي على المكدس. |
| [set_Bold](./set_bold/)(bool) | معين لـ [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | معين لـ [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | معين لـ [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | المحدد لـ [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | يحدد الموضع الحالي في المستند كبداية إشارة مرجعية. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | يحدد الموضع الحالي في المستند كبداية إشارة مرجعية للعمود. يجب أن يكون الموضع داخل خلية جدول. |
| [StartEditableRange](./starteditablerange/)() | يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير. |
| [StartTable](./starttable/)() | يبدأ جدولًا في المستند. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | يدرج سلسلة نصية في المستند عند موضع الإدراج الحالي. |
| [Writeln](./writeln/)(const System::String\&) | يدرج سلسلة نصية وفاصل فقرة في المستند. |
| [Writeln](./writeln/)() | يقوم بإدراج فاصل فقرة في المستند. |
## ملاحظات


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

أنشئ [DocumentBuilder](./) واربطه بـ [Document](../document/).

يحتوي [DocumentBuilder](./) على مؤشر داخلي حيث سيتم إدراج النص عندما تستدعي [Write()](../)، [Writeln()](../)، [InsertBreak()](./insertbreak/) وغيرها من الطرق. يمكنك تحريك مؤشر [DocumentBuilder](./) إلى موقع مختلف في المستند باستخدام طرق MoveToXXX المتنوعة.

استخدم خاصية [Font](./get_font/) لتحديد تنسيق الأحرف الذي سيُطبق على جميع النصوص المُدرجة من الموضع الحالي في المستند فصاعدًا.

استخدم خاصية [ParagraphFormat](./get_paragraphformat/) لتحديد تنسيق الفقرات للموقع الحالي وجميع الفقرات التي سيتم إدراجها.

استخدم خاصية [PageSetup](./get_pagesetup/) لتحديد خصائص الصفحة والقسم للقسم الحالي وجميع الأقسام التي سيتم إدراجها.

استخدم خاصيتي [CellFormat](./get_cellformat/) و[RowFormat](./get_rowformat/) لتحديد خصائص التنسيق لخلايا الجدول والصفوف. استخدم طرق [InsertCell](./insertcell/) و[EndRow](./endrow/) لبناء جدول.

لاحظ أن خصائص [Font](./get_font/)، [ParagraphFormat](./get_paragraphformat/) و[PageSetup](./get_pagesetup/) يتم تحديثها كلما انتقلت إلى موقع مختلف في المستند لتعكس خصائص التنسيق المتاحة في الموقع الجديد.

## أمثلة



يوضح كيفية بناء جدول بحدود مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// تعيين خيارات تنسيق الجدول لمنشئ المستند
// سيتم تطبيقها على كل صف وخلية نضيفها به.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// تغيير التنسيق سيطبقه على الخلية الحالية،
// وأي خلايا جديدة ننشئها باستخدام المنشئ لاحقًا.
// هذا لن يؤثر على الخلايا التي أضفناها مسبقًا.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// زد ارتفاع الصف لتناسب النص العمودي.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


يوضح كيفية استخدام منشئ المستند لإنشاء جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// ابدأ الجدول، ثم املأ الصف الأول بخليةين.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// استدعِ طريقة "EndRow" للمنشئ لبدء صف جديد.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
