---
title: "Класс Aspose::Words::DocumentBuilder"
linktitle: "DocumentBuilder"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::DocumentBuilder. Предоставляет методы для вставки текста, изображений и другого содержимого, указания форматирования шрифтов, абзацев и разделов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Предоставляет методы для вставки текста, изображений и другого содержимого, указания шрифта, форматирования абзацев и разделов. Чтобы узнать больше, посетите статью документации [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/).

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Удаляет строку из таблицы. |
| [DocumentBuilder](./documentbuilder/)() | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Инициализирует новый экземпляр этого класса. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Помечает текущую позицию в документе как конец закладки. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Помечает текущую позицию в документе как конец закладки столбца. Позиция должна находиться в ячейке таблицы. |
| [EndEditableRange](./endeditablerange/)() | Помечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Помечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndRow](./endrow/)() | Завершает строку таблицы в документе. |
| [EndTable](./endtable/)() | Завершает таблицу в документе. |
| [get_Bold](./get_bold/)() | True, если шрифт оформлен как полужирный. |
| [get_CellFormat](./get_cellformat/)() | Возвращает объект, представляющий текущие свойства форматирования ячейки таблицы. |
| [get_CurrentNode](./get_currentnode/)() | Получает узел, который в данный момент выбран в этом [DocumentBuilder](./). |
| [get_CurrentParagraph](./get_currentparagraph/)() | Получает абзац, который в данный момент выбран в этом [DocumentBuilder](./). |
| [get_CurrentSection](./get_currentsection/)() | Получает раздел, который в данный момент выбран в этом [DocumentBuilder](./). |
| [get_CurrentStory](./get_currentstory/)() | Получает историю, которая в данный момент выбрана в этом [DocumentBuilder](./). |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Получает структурированный тег документа, который в данный момент выбран в этом [DocumentBuilder](./). |
| [get_Document](./get_document/)() const | Получает или задает объект [Document](./get_document/), к которому прикреплен данный объект. |
| [get_Font](./get_font/)() | Возвращает объект, представляющий текущие свойства форматирования шрифта. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | Возвращает **true**, если курсор находится в конце текущего абзаца. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | Возвращает **true**, если курсор находится в конце структурированного тега документа. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | Возвращает **true**, если курсор находится в начале текущего абзаца (текст перед курсором отсутствует). |
| [get_Italic](./get_italic/)() | True, если шрифт оформлен курсивом. |
| [get_ListFormat](./get_listformat/)() | Возвращает объект, представляющий текущие свойства форматирования списка. |
| [get_PageSetup](./get_pagesetup/)() | Возвращает объект, представляющий текущие настройки страницы и свойства раздела. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Возвращает объект, представляющий текущие свойства форматирования абзаца. |
| [get_RowFormat](./get_rowformat/)() | Возвращает объект, представляющий текущие свойства форматирования строки таблицы. |
| [get_Underline](./get_underline/)() | Получает/устанавливает тип подчеркивания для текущего шрифта. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Вставляет разрыв указанного типа в документ. |
| [InsertCell](./insertcell/)() | Вставляет ячейку таблицы в документ. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Вставляет поле формы с флажком в текущую позицию. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Вставляет поле формы с флажком в текущую позицию. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Вставляет поле формы с выпадающим списком в текущую позицию. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Вставляет документ в позицию курсора. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Вставляет документ в позицию курсора. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Вставляет документ встроенно в позицию курсора. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Вставляет поле Word в документ и при необходимости обновляет результат поля. |
| [InsertField](./insertfield/)(const System::String\&) | Вставляет поле Word в документ и обновляет результат поля. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Вставляет поле Word в документ без обновления результата поля. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Вставляет сноску или концевую сноску в документ. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Вставляет сноску или концевую сноску в документ. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Вставляет объект [Forms2OleControl](../) в текущую позицию. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Группирует переданные в параметре фигуры в новый узел GroupShape, который вставляется в текущую позицию. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Группирует переданные в параметре фигуры в новый узел GroupShape указанного размера, который вставляется в указанную позицию. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Вставляет форму горизонтальной линии в документ. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Вставляет строку HTML в документ. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Вставляет строку HTML в документ. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Вставляет строку HTML в документ. Позволяет указать дополнительные параметры. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Вставляет гиперссылку в документ. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Вставляет изображение из объекта **Image** в документ. Изображение вставляется встроенно и с масштабом 100%. |
| [InsertImage](./insertimage/)(const System::String\&) | Вставляет изображение из файла или URL в документ. Изображение вставляется встроенно и с масштабом 100%. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Вставляет изображение из потока в документ. Изображение вставляется встроенно и с масштабом 100%. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Вставляет изображение из массива байтов в документ. Изображение вставляется встроенно и с масштабом 100%. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | Вставляет встроенное изображение из объекта **Image** в документ и масштабирует его до указанного размера. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Вставляет встроенное изображение из файла или URL в документ и масштабирует его до указанного размера. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Вставляет встроенное изображение из потока в документ и масштабирует его до указанного размера. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Вставляет встроенное изображение из массива байтов в документ и масштабирует его до указанного размера. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет изображение из объекта **Image** в указанную позицию и размер. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет изображение из файла или URL в указанную позицию и размер. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет изображение из потока в указанную позицию и размер. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет изображение из массива байтов в указанную позицию и размер. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел перед курсором. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Вставляет встроенный объект OLE из потока в документ. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE с помощью расширения файла. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE с помощью указанного параметра progID. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Вставляет встроенный или связанный объект OLE в виде значка в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с помощью расширения файла. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Вставляет встроенный или связанный объект OLE в виде значка в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с помощью указанного параметра progID. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Вставляет встроенный объект OLE в виде значка из потока в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с помощью указанного параметра progID. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет онлайн‑видео объект в документ и масштабирует его до указанного размера. |
| [InsertParagraph](./insertparagraph/)() | Вставляет разрыв абзаца в документ. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Вставляет встроенную форму с указанным типом и размером. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Вставляет плавающую форму с указанным положением, размером и типом обтекания текста. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Вставляет строку подписи в текущую позицию. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Вставляет строку подписи в указанную позицию. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Вставляет [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) в документ. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Вставляет разделитель стилей в документ. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Вставляет поле TOC (оглавление) в документ. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Вставляет текстовое поле формы в текущую позицию. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Перемещает курсор к встроенному узлу или в конец абзаца. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | Перемещает курсор к закладке. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | Перемещает курсор к закладке с большей точностью. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | Перемещает курсор к ячейке таблицы в текущем разделе. |
| [MoveToDocumentEnd](./movetodocumentend/)() | Перемещает курсор в конец документа. |
| [MoveToDocumentStart](./movetodocumentstart/)() | Перемещает курсор в начало документа. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | Перемещает курсор к полю в документе. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | Перемещает курсор в начало колонтитула или нижнего колонтитула в текущем разделе. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | Перемещает курсор в позицию сразу после указанного поля слияния и удаляет поле слияния. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Перемещает поле слияния в указанное поле слияния. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | Перемещает курсор к абзацу в текущем разделе. |
| [MoveToSection](./movetosection/)(int32_t) | Перемещает курсор в начало тела в указанном разделе. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | Перемещает курсор к структурному тегу документа в текущем разделе. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | Перемещает курсор к структурному тегу документа. |
| [PopFont](./popfont/)() | Получает форматирование символов, ранее сохранённое в стеке. |
| [PushFont](./pushfont/)() | Сохраняет текущее форматирование символов в стек. |
| [set_Bold](./set_bold/)(bool) | Сеттер для [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Сеттер для [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Сеттер для [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Сеттер для [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | Помечает текущую позицию в документе как начало закладки. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Помечает текущую позицию в документе как начало столбцовой закладки. Позиция должна находиться в ячейке таблицы. |
| [StartEditableRange](./starteditablerange/)() | Помечает текущую позицию в документе как начало редактируемого диапазона. |
| [StartTable](./starttable/)() | Начинает таблицу в документе. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Вставляет строку в документ в текущую позицию вставки. |
| [Writeln](./writeln/)(const System::String\&) | Вставляет строку и разрыв абзаца в документ. |
| [Writeln](./writeln/)() | Вставляет разрыв абзаца в документ. |
## Примечания


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Создайте [DocumentBuilder](./) и свяжите его с [Document](../document/).

У [DocumentBuilder](./) есть внутренний курсор, в который будет вставляться текст при вызове [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) и других методов. Вы можете перемещать курсор [DocumentBuilder](./) в другое место документа, используя различные методы MoveToXXX.

Используйте свойство [Font](./get_font/) для указания форматирования символов, которое будет применяться ко всему тексту, вставляемому с текущей позиции в документе и далее.

Используйте свойство [ParagraphFormat](./get_paragraphformat/) для указания форматирования абзацев для текущего и всех последующих вставляемых абзацев.

Используйте свойство [PageSetup](./get_pagesetup/) для указания параметров страницы и раздела для текущего раздела и всех последующих вставляемых разделов.

Используйте свойства [CellFormat](./get_cellformat/) и [RowFormat](./get_rowformat/) для указания параметров форматирования ячеек таблицы и строк. Используйте методы [InsertCell](./insertcell/) и [EndRow](./endrow/) для построения таблицы.

Обратите внимание, что свойства [Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) и [PageSetup](./get_pagesetup/) обновляются каждый раз, когда вы перемещаетесь в другое место документа, чтобы отразить доступные в новой позиции параметры форматирования.

## Примеры



Показывает, как построить таблицу с пользовательскими границами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Установка параметров форматирования таблицы для DocumentBuilder
// будет применять их к каждой строке и ячейке, которые мы добавляем с его помощью.
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

// Изменение форматирования будет применено к текущей ячейке,
// и к любым новым ячейкам, которые мы создаём с помощью билдера позже.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Увеличьте высоту строки, чтобы разместить вертикальный текст.
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


Показывает, как использовать DocumentBuilder для создания таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Начните таблицу, затем заполните первую строку двумя ячейками.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Вызовите метод билдера "EndRow", чтобы начать новую строку.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
