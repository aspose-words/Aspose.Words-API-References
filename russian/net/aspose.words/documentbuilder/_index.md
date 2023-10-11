---
title: Class DocumentBuilder
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.DocumentBuilder сорт. Предоставляет методы для вставки текста изображений и другого содержимого указания шрифта форматирования абзацев и разделов.
type: docs
weight: 450
url: /ru/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Предоставляет методы для вставки текста, изображений и другого содержимого, указания шрифта, форматирования абзацев и разделов.

Чтобы узнать больше, посетите[Обзор конструктора документов](https://docs.aspose.com/words/net/document-builder-overview/) статья документации.

```csharp
public class DocumentBuilder
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | True, если шрифт отформатирован как жирный. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Возвращает объект, который представляет свойства форматирования текущей ячейки таблицы. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Получает узел, выбранный в данный момент в этом DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Получает абзац, выбранный в данный момент в этом`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Получает раздел, выбранный в данный момент в этом`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Получает историю, выбранную в данный момент в этом`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Получает тег структурированного документа, выбранный в данный момент в этом`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Получает или задает[`Document`](./document/)объект, к которому прикреплен этот объект. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Возвращает объект, представляющий текущие свойства форматирования шрифта. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Возвращает`истинный` если курсор находится в конце текущего абзаца. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Возвращает **истинный** если курсор находится в конце тега структурированного документа. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Возвращает`истинный` если курсор находится в начале текущего абзаца (нет текста перед курсором). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | True, если шрифт отформатирован как курсив. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Возвращает объект, который представляет свойства форматирования текущего списка. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Возвращает объект, который представляет текущие настройки страницы и свойства раздела. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Возвращает объект, представляющий текущие свойства форматирования абзаца. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Возвращает объект, который представляет свойства форматирования текущей строки таблицы. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Получает/устанавливает тип подчеркивания для текущего шрифта. |

## Методы

| Имя | Описание |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Удаляет строку из таблицы. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Отмечает текущую позицию в документе как конец закладки. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна находиться в ячейке таблицы. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Отмечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Отмечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Завершает строку таблицы в документе. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Завершает таблицу в документе. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Вставляет в документ разрыв указанного типа. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Вставляет ячейку таблицы в документ. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Вставляет поле формы флажка в текущую позицию. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Вставляет поле формы флажка в текущую позицию. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Вставляет поле формы со списком в текущую позицию. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | Вставляет документ в позицию курсора. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Вставляет документ в позицию курсора. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Вставляет поле Word в документ и обновляет результат поля. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Вставляет поле Word в документ и при необходимости обновляет результат поля. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Вставляет поле Word в документ без обновления результата поля. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Вставляет в документ сноску или концевую сноску. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Вставляет в документ сноску или концевую сноску. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Вставляет в документ фигуру горизонтальной линейки. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Вставляет в документ HTML-строку. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Вставляет в документ HTML-строку. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Вставляет в документ строку HTML. Позволяет указать дополнительные параметры. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Вставляет гиперссылку в документ. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Вставляет в документ изображение из байтового массива. Изображение вставляется встроенным в масштаб 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | Вставляет изображение из .NET.Image в документ. Изображение вставляется встроенным в масштаб 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Вставляет изображение из потока в документ. Изображение вставляется встроенным в масштаб 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Вставляет изображение из файла или URL-адреса в документ. Изображение вставляется встроенным в масштаб 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Вставляет в документ встроенное изображение из байтового массива и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | Вставляет встроенное изображение из .NET.Image объект в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Вставляет встроенное изображение из потока в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Вставляет встроенное изображение из файла или URL-адреса в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из байтового массива в указанную позицию и размер. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из .NET.ImageОбъект в указанном положении и размере. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из потока в указанную позицию и размер. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из файла или URL-адреса в указанную позицию и размер. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | Вставляет узел перед курсором. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Вставляет внедренный объект OLE из потока в документ. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Вставляет внедренный или связанный объект OLE из файла в документ. Обнаруживает тип объекта OLE по расширению файла. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Вставляет внедренный или связанный объект OLE из файла в документ. Обнаруживает тип объекта OLE, используя заданный параметр progID. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Вставляет внедренный объект OLE в виде значка из потока в документ. Позволяет указать файл значка и заголовок. Обнаруживает тип объекта OLE, используя заданный параметр progID. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Вставляет встроенный или связанный объект OLE в качестве значка в документ. Позволяет указать файл значка и заголовок. Обнаруживает тип объекта OLE по расширению файла. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Вставляет встроенный или связанный объект OLE в качестве значка в документ. Позволяет указать файл значка и заголовок. Обнаруживает тип объекта OLE, используя заданный параметр progID. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Вставляет в документ разрыв абзаца. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Вставляет встроенную фигуру указанного типа и размера. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет свободно плавающую фигуру с указанным положением, размером и типом переноса текста. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Вставляет строку подписи в текущую позицию. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Вставляет строку подписи в указанную позицию. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Вставляет в документ разделитель стилей. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Вставляет поле TOC (оглавление) в документ. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Вставляет поле текстовой формы в текущую позицию. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | Перемещает курсор к строчному узлу или в конец абзаца. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | Перемещает курсор на закладку. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | Перемещает курсор к закладке с большей точностью. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | Перемещает курсор в ячейку таблицы в текущем разделе. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Перемещает курсор в конец документа. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Перемещает курсор в начало документа. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | Перемещает курсор в поле документа. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | Перемещает курсор в начало верхнего или нижнего колонтитула текущего раздела. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | Перемещает курсор в позицию сразу за указанным полем слияния и удаляет поле слияния. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Перемещает поле слияния в указанное поле слияния. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | Перемещает курсор на абзац текущего раздела. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | Перемещает курсор в начало тела указанного раздела. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | Перемещает курсор на тег структурированного документа в текущем разделе. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | Перемещает курсор к тегу структурированного документа. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Извлекает форматирование символов, ранее сохраненное в стеке. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Сохраняет текущее форматирование символов в стек. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Отмечает текущую позицию в документе как начало закладки. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна находиться в ячейке таблицы. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Отмечает текущую позицию в документе как начало редактируемого диапазона. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Начинает таблицу в документе. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Вставляет строку в документ в текущую позицию вставки. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Вставляет в документ разрыв абзаца. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Вставляет в документ строку и разрыв абзаца. |

### Примечания

`DocumentBuilder` делает процесс построения[`Document`](../document/) проще. [`Document`](../document/) представляет собой составной объект, состоящий из дерева узлов, и хотя вставка узлов content возможна непосредственно в дерево, это требует хорошего понимания древовидной структуры. `DocumentBuilder` является «фасадом» сложной структуры[`Document`](../document/) и позволяет быстро и легко вставлять контент и форматировать.

Создать`DocumentBuilder` и связать его с[`Document`](../document/).

`DocumentBuilder` имеет внутренний курсор, куда будет вставлен текст при вызове[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) и другие методы. Вы можете перемещаться по`DocumentBuilder` курсор в другое место в документе, используя различные методы MoveToXXX.

Использовать[`Font`](./font/)Свойство, позволяющее указать форматирование символов, которое будет применяться к ко всему тексту, вставленному начиная с текущей позиции в документе.

Использовать[`ParagraphFormat`](./paragraphformat/) свойство, позволяющее указать форматирование абзаца для current и всех абзацев, которые будут вставлены.

Использовать[`PageSetup`](./pagesetup/) Свойство для указания свойств страницы и раздела для раздела current и всего раздела, который будет вставлен.

Использовать[`CellFormat`](./cellformat/) и[`RowFormat`](./rowformat/) свойства для указания свойств форматирования для ячеек и строк таблицы. Пользователь[`InsertCell`](./insertcell/) and [`EndRow`](./endrow/) методы построения таблицы.

Обратите внимание, что[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) и[`PageSetup`](./pagesetup/) свойства обновляются всякий раз, когда вы переходите в другое место документа, чтобы отразить свойства форматирования, доступные в новом месте.

### Примеры

Показывает, как использовать построитель документов для создания таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Запускаем таблицу, затем заполняем первую строку двумя ячейками.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Вызов метода построителя «EndRow», чтобы начать новую строку.
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

// Указываем, что нам нужны разные верхние и нижние колонтитулы для первой, четной и нечетной страниц.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Создайте заголовки, затем добавьте в документ три страницы для отображения каждого типа заголовка.
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

Показывает, как создать таблицу с настраиваемыми границами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для построителя документов
// будет применять их к каждой строке и ячейке, которые мы добавляем вместе с ними.
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

// При изменении форматирования оно будет применено к текущей ячейке,
// и любые новые ячейки, которые мы создадим впоследствии с помощью построителя.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Увеличиваем высоту строки, чтобы она соответствовала вертикальному тексту.
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


