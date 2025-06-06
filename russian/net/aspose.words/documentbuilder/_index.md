---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.DocumentBuilder — ваше решение для легкой вставки текста, изображений и элементов форматирования в документы.
type: docs
weight: 660
url: /ru/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Предоставляет методы для вставки текста, изображений и другого контента, указания шрифта, форматирования абзацев и разделов.

Чтобы узнать больше, посетите[Обзор конструктора документов](https://docs.aspose.com/words/net/document-builder-overview/) документальная статья.

```csharp
public class DocumentBuilder
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | True, если шрифт отформатирован как жирный. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Возвращает объект, представляющий текущие свойства форматирования ячейки таблицы. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Получает узел, который в данный момент выбран в этом DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Получает абзац, который в данный момент выбран в этом`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Получает раздел, который в данный момент выбран в этом`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Получает историю, которая в данный момент выбрана в этом`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Получает структурированный тег документа, который в данный момент выбран в этом`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Получает или задает[`Document`](./document/) объект, к которому прикреплен этот объект. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Возвращает объект, представляющий текущие свойства форматирования шрифта. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Возврат`истинный` если курсор находится в конце текущего абзаца. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Возврат**истинный** если курсор находится в конце структурированного документа тег. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Возврат`истинный`если курсор находится в начале текущего абзаца (перед курсором нет текста). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | True, если шрифт отформатирован как курсив. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Возвращает объект, представляющий текущие свойства форматирования списка. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Возвращает объект, представляющий текущие настройки страницы и свойства раздела. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Возвращает объект, представляющий текущие свойства форматирования абзаца. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Возвращает объект, представляющий текущие свойства форматирования строки таблицы. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Получает/устанавливает тип подчеркивания для текущего шрифта. |

## Методы

| Имя | Описание |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | Удаляет строку из таблицы. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | Отмечает текущую позицию в документе как конец закладки. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна быть в ячейке таблицы. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Отмечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | Отмечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Завершает строку таблицы в документе. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Завершает таблицу в документе. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | Вставляет разрыв указанного типа в документ. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Вставляет ячейку таблицы в документ. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | Вставляет поле формы флажка в текущую позицию. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | Вставляет поле формы флажка в текущую позицию. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | Вставляет поле формы со списком в текущую позицию. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | Вставляет документ в позицию курсора. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Вставляет документ в позицию курсора. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Вставляет документ в позицию курсора. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | Вставляет поле Word в документ и обновляет результат поля. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Вставляет поле Word в документ и при необходимости обновляет результат поля. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | Вставляет поле Word в документ без обновления результата поля. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | Вставляет сноску или концевую сноску в документ. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | Вставляет сноску или концевую сноску в документ. |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | Вставки[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/) объект в текущую позицию. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | Группирует фигуры, переданные в качестве параметра, в новый узел GroupShape, который вставляется в текущую позицию. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | Группирует фигуры, переданные в качестве параметра, в новый узел GroupShape указанного размера, который вставляется в указанную позицию. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Вставляет в документ горизонтальную линейку. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | Вставляет HTML-строку в документ. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | Вставляет HTML-строку в документ. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | Вставляет HTML-строку в документ. Позволяет указать дополнительные параметры. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | Вставляет гиперссылку в документ. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | Вставляет изображение из массива байтов в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | Вставляет изображение из .NETImage Объект в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | Вставляет изображение из потока в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | Вставляет изображение из файла или URL в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | Вставляет встроенное изображение из байтового массива в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | Вставляет встроенное изображение из .NETImage объект в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | Вставляет встроенное изображение из потока в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | Вставляет встроенное изображение из файла или URL в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет изображение из массива байтов в указанную позицию и размер. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет изображение из .NETImage Объект в указанном положении и размере. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет изображение из потока в указанную позицию и размер. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет изображение из файла или URL в указанное положение и размер. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | Вставляет узел перед курсором. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | Вставляет внедренный OLE-объект из потока в документ. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE по расширению файла. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE с использованием заданного параметра progID. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | Вставляет встроенный объект OLE как значок из потока в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с использованием заданного параметра progID. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | Вставляет встроенный или связанный объект OLE как значок в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE по расширению файла. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | Вставляет встроенный или связанный объект OLE как значок в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с использованием заданного параметра progID. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | Вставляет онлайн-видеообъект в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | Вставляет онлайн-видеообъект в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет онлайн-видеообъект в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет онлайн-видеообъект в документ и масштабирует его до указанного размера. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Вставляет разрыв абзаца в документ. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | Вставляет встроенную фигуру указанного типа и размера. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет свободно плавающую фигуру с указанным положением, размером и типом обтекания текстом. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | Вставляет строку подписи в текущую позицию. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Вставляет строку подписи в указанную позицию. |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | Вставляет[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) в документ. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Вставляет разделитель стилей в документ. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | Вставляет поле TOC (оглавление) в документ. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | Вставляет поле текстовой формы в текущую позицию. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | Перемещает курсор на встроенный узел или в конец абзаца. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | Перемещает курсор на закладку. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | Перемещает курсор на закладку с большей точностью. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | Перемещает курсор в ячейку таблицы в текущем разделе. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Перемещает курсор в конец документа. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Перемещает курсор в начало документа. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | Перемещает курсор в поле в документе. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | Перемещает курсор в начало верхнего или нижнего колонтитула в текущем разделе. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | Перемещает курсор в положение сразу за указанным полем слияния и удаляет поле слияния. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | Перемещает поле слияния в указанное поле слияния. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | Перемещает курсор на абзац в текущем разделе. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | Перемещает курсор в начало тела в указанном разделе. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | Перемещает курсор на структурированный тег документа в текущем разделе. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | Перемещает курсор к тегу структурированного документа. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Извлекает форматирование символов, ранее сохраненное в стеке. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Сохраняет текущее форматирование символов в стеке. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | Отмечает текущую позицию в документе как начало закладки. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна быть в ячейке таблицы. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Отмечает текущую позицию в документе как начало редактируемого диапазона. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Начинает таблицу в документе. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | Вставляет строку в документ в текущую позицию вставки. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Вставляет разрыв абзаца в документ. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | Вставляет строку и разрыв абзаца в документ. |

## Примечания

`DocumentBuilder` делает процесс строительства[`Document`](../document/) проще. [`Document`](../document/) представляет собой составной объект, состоящий из дерева узлов, и хотя вставка узлов content непосредственно в дерево возможна, для этого требуется хорошее понимание структуры дерева. `DocumentBuilder` является «фасадом» для сложной структуры[`Document`](../document/) и позволяет быстро и легко вставлять контент и форматирование.

Создать`DocumentBuilder` и свяжите его с[`Document`](../document/).

The`DocumentBuilder` имеет внутренний курсор, куда будет вставлен текст при вызове[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) и другие методы. Вы можете перемещаться по`DocumentBuilder` курсор в другое местоположение в документе с помощью различных методов MoveToXXX.

Используйте[`Font`](./font/) свойство для указания форматирования символов, которое будет применяться ко всему тексту, вставленному с текущей позиции в документе и далее.

Используйте[`ParagraphFormat`](./paragraphformat/) свойство для указания форматирования абзаца для current и всех абзацев, которые будут вставлены.

Используйте[`PageSetup`](./pagesetup/) свойство для указания свойств страницы и раздела для раздела current и всех разделов, которые будут вставлены.

Используйте[`CellFormat`](./cellformat/) и[`RowFormat`](./rowformat/) свойства для указания свойств форматирования для ячеек и строк таблицы. Пользователь[`InsertCell`](./insertcell/) и [`EndRow`](./endrow/) методы построения таблицы.

Обратите внимание, что[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) и[`PageSetup`](./pagesetup/) свойства обновляются всякий раз, когда вы переходите в другое место документа, чтобы отразить свойства форматирования, доступные в новом месте.

## Примеры

Показывает, как использовать конструктор документов для создания таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Запускаем таблицу, затем заполняем первую строку двумя ячейками.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Вызываем метод «EndRow» конструктора, чтобы начать новую строку.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Показывает, как создавать верхние и нижние колонтитулы в документе с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите, что нам нужны разные верхние и нижние колонтитулы для первой, четной и нечетной страниц.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Создаем заголовки, затем добавляем в документ три страницы для отображения каждого типа заголовков.
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

Показывает, как создать таблицу с пользовательскими границами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Настройка параметров форматирования таблиц для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавим вместе с ним.
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

// Изменение форматирования применится к текущей ячейке,
// и любые новые ячейки, которые мы создадим с помощью конструктора впоследствии.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Увеличиваем высоту строки, чтобы вместить вертикальный текст.
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

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
