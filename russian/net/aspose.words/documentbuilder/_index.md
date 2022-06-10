---
title: DocumentBuilder
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет методы для вставки текста изображений и другого содержимого определения шрифта форматирования абзаца и раздела.
type: docs
weight: 440
url: /ru/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Предоставляет методы для вставки текста, изображений и другого содержимого, определения шрифта, форматирования абзаца и раздела.

```csharp
public class DocumentBuilder
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DocumentBuilder](documentbuilder#constructor)() | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder](documentbuilder#constructor_1)(Document) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold) { get; set; } | Истинно, если шрифт отформатирован как полужирный. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat) { get; } | Возвращает объект, представляющий текущие свойства форматирования ячейки таблицы. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode) { get; } | Получает узел, выбранный в данный момент в этом DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph) { get; } | Получает абзац, выбранный в данный момент в этом DocumentBuilder. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection) { get; } | Получает раздел, выбранный в данный момент в этом DocumentBuilder. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory) { get; } | Получает историю, выбранную в данный момент в этом DocumentBuilder. |
| [Document](../../aspose.words/documentbuilder/document) { get; set; } | Получает или задает объект[`Document`](./document), к которому присоединен этот объект. |
| [Font](../../aspose.words/documentbuilder/font) { get; } | Возвращает объект, представляющий текущие свойства форматирования шрифта. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph) { get; } | Возвращает true, если курсор находится в конце текущего абзаца. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph) { get; } | Возвращает true, если курсор находится в начале текущего абзаца (перед курсором нет текста). |
| [Italic](../../aspose.words/documentbuilder/italic) { get; set; } | Истинно, если шрифт отформатирован как курсив. |
| [ListFormat](../../aspose.words/documentbuilder/listformat) { get; } | Возвращает объект, представляющий текущие свойства форматирования списка. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup) { get; } | Возвращает объект, представляющий текущую настройку страницы и свойства раздела. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat) { get; } | Возвращает объект, представляющий текущие свойства форматирования абзаца. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat) { get; } | Возвращает объект, представляющий текущие свойства форматирования строки таблицы. |
| [Underline](../../aspose.words/documentbuilder/underline) { get; set; } | Получает/устанавливает тип подчеркивания для текущего шрифта. |

## Методы

| Имя | Описание |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow)(int, int) | Удаляет строку из таблицы. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark)(string) | Отмечает текущую позицию в документе как конец закладки. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark)(string) | Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна быть в ячейке таблицы. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange#endeditablerange)() | Отмечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange#endeditablerange_1)(EditableRangeStart) | Отмечает текущую позицию в документе как конец редактируемого диапазона. |
| [EndRow](../../aspose.words/documentbuilder/endrow)() | Завершает строку таблицы в документе. |
| [EndTable](../../aspose.words/documentbuilder/endtable)() | Завершает таблицу в документе. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak)(BreakType) | Вставляет в документ разрыв указанного типа. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell)() | Вставляет ячейку таблицы в документ. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart#insertchart_1)(ChartType, double, double) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет объект диаграммы в документ и масштабирует его до указанного размера. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox#insertcheckbox_1)(string, bool, int) | Вставляет поле формы флажка в текущую позицию. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox#insertcheckbox)(string, bool, bool, int) | Вставляет поле формы флажка в текущую позицию. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox)(string, string[], int) | Вставляет поле формы со списком в текущую позицию. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument#insertdocument)(Document, ImportFormatMode) | Вставляет документ в позицию курсора. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Вставляет документ в позицию курсора. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield_1)(string) | Вставляет поле Word в документ и обновляет результат поля. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield)(FieldType, bool) | Вставляет поле Word в документ и при необходимости обновляет результат поля. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield_2)(string, string) | Вставляет поле Word в документ без обновления результата поля. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote#insertfootnote)(FootnoteType, string) | Вставляет сноску или концевую сноску в документ. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote#insertfootnote_1)(FootnoteType, string, string) | Вставляет сноску или концевую сноску в документ. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule)() | Вставляет в документ форму горизонтальной линейки. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml)(string) | Вставляет строку HTML в документ. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml_2)(string, bool) | Вставляет строку HTML в документ. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml_1)(string, HtmlInsertOptions) | Вставляет строку HTML в документ. Позволяет указать дополнительные параметры. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink)(string, string, bool) | Вставляет гиперссылку в документ. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage)(byte[]) | Вставляет изображение из байтового массива в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_3)(Image) | Вставляет изображение из .NETImage объект в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_6)(Stream) | Вставляет изображение из потока в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_9)(string) | Вставляет изображение из файла или URL-адреса в документ. Изображение вставляется в строку и в масштабе 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_2)(byte[], double, double) | Вставляет встроенное изображение из байтового массива в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_5)(Image, double, double) | Вставляет встроенное изображение из объекта .NETImage в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_8)(Stream, double, double) | Вставляет встроенное изображение из потока в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_11)(string, double, double) | Вставляет встроенное изображение из файла или URL-адреса в документ и масштабирует его до указанного размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из байтового массива в указанной позиции и размера. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из объекта .NETImage в указанную позицию и размер. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из потока в указанной позиции и размере. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет изображение из файла или URL-адреса в указанной позиции и размере. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode)(Node) | Вставляет узел текстового уровня внутри текущего абзаца перед курсором. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject)(Stream, string, bool, Stream) | Вставляет встроенный объект OLE из потока в документ. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject_1)(string, bool, bool, Stream) | Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE, используя расширение файла. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject_2)(string, string, bool, bool, Stream) | Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE, используя заданный параметр progID. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon)(Stream, string, string, string) | Вставляет встроенный объект OLE в качестве значка из потока в документ. Позволяет указать файл иконки и заголовок. Определяет тип объекта OLE, используя заданный параметр progID. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon_1)(string, bool, string, string) | Вставляет встроенный или связанный объект OLE в качестве значка в документ. Позволяет указать файл иконки и заголовок. Определяет тип объекта OLE, используя расширение файла. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon_2)(string, string, bool, string, string) | Вставляет встроенный или связанный объект OLE в качестве значка в документ. Позволяет указать файл иконки и заголовок. Определяет тип объекта OLE, используя заданный параметр progID. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_1)(string, double, double) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_3)(string, string, byte[], double, double) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph)() | Вставляет разрыв абзаца в документ. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape#insertshape_1)(ShapeType, double, double) | Вставляет встроенную фигуру указанного типа и размера. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Вставляет свободно плавающую фигуру с указанным положением, размером и типом обтекания текстом. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline#insertsignatureline)(SignatureLineOptions) | Вставляет строку подписи в текущую позицию. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Вставляет строку подписи в указанную позицию. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator)() | Вставляет разделитель стилей в документ. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents)(string) | Вставляет в документ поле TOC (оглавление). |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput)(string, TextFormFieldType, string, string, int) | Вставляет поле текстовой формы в текущую позицию. |
| [MoveTo](../../aspose.words/documentbuilder/moveto)(Node) | Перемещает курсор на встроенный узел или в конец абзаца. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark#movetobookmark)(string) | Перемещает курсор на закладку. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark#movetobookmark_1)(string, bool, bool) | Перемещает курсор к закладке с большей точностью. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell)(int, int, int, int) | Перемещает курсор в ячейку таблицы в текущем разделе. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend)() | Перемещает курсор в конец документа. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart)() | Перемещает курсор в начало документа. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield)(Field, bool) | Перемещает курсор в поле документа. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter)(HeaderFooterType) | Перемещает курсор в начало верхнего или нижнего колонтитула в текущем разделе. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield#movetomergefield)(string) | Перемещает курсор в положение сразу за указанным полем слияния и удаляет поле слияния. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield#movetomergefield_1)(string, bool, bool) | Перемещает поле слияния в указанное поле слияния. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph)(int, int) | Перемещает курсор на абзац в текущем разделе. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection)(int) | Перемещает курсор в начало тела в указанном разделе. |
| [PopFont](../../aspose.words/documentbuilder/popfont)() | Извлекает форматирование символов, ранее сохраненное в стеке. |
| [PushFont](../../aspose.words/documentbuilder/pushfont)() | Сохраняет текущее форматирование символов в стек. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark)(string) | Отмечает текущую позицию в документе как начало закладки. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark)(string) | Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна быть в ячейке таблицы. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange)() | Помечает текущую позицию в документе как начало редактируемого диапазона. |
| [StartTable](../../aspose.words/documentbuilder/starttable)() | Запускает таблицу в документе. |
| [Write](../../aspose.words/documentbuilder/write)(string) | Вставляет строку в документ в текущей позиции вставки. |
| [Writeln](../../aspose.words/documentbuilder/writeln#writeln)() | Вставляет разрыв абзаца в документ. |
| [Writeln](../../aspose.words/documentbuilder/writeln#writeln_1)(string) | Вставляет в документ строку и разрыв абзаца. |

### Примечания

**DocumentBuilder** делает Процесс создания **документа** проще.  **Document** представляет собой составной объект, состоящий из дерева узлов и при вставке содержимого узлов непосредственно в дерево возможно, это требует хорошего понимания структуры дерева.  **DocumentBuilder** является «фасадом» сложной структуры **Document** и позволяет быстро и легко вставлять содержимое и форматирование.

Создайте **DocumentBuilder** и свяжите его сДокумент.

**DocumentBuilder** имеет внутренний курсор, куда будет вставлен текст при вызове[`Write`](./write),[`Writeln`](./writeln),[`InsertBreak`](./insertbreak) и другие методы. Вы можете перемещать курсор **DocumentBuilder** в другое место в документе, используя различные методы MoveToXXX.

Используйте свойство[`Font`](./font)для указания форматирования символов, которое будет применяться к весь текст, вставленный с текущей позиции в документе и далее.

Используйте свойство[`ParagraphFormat`](./paragraphformat)для указания форматирования абзаца для текущего и все абзацы, которые будут вставлены.

Используйте свойство[`PageSetup`](./pagesetup)для указания свойств страницы и раздела для текущего раздел и весь раздел, который будет вставлен.

Используйте[`CellFormat`](./cellformat)и[`RowFormat`](./rowformat)свойства для указания свойств форматирования для ячеек и строк таблицы. Используйте методы[`InsertCell`](./insertcell)и [`EndRow`](./endrow)для построения таблицы.

Обратите внимание, что **Font** , **ParagraphFormat**: и **PageSetup** свойства обновляются всякий раз, когда вы переходите в другое место в документе, чтобы отразить свойства форматирования, доступные в новом месте .

### Примеры

Показывает, как использовать конструктор документов для создания таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавляем вместе с ней.
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

// Изменение форматирования применит его к текущей ячейке,
// и любые новые ячейки, которые мы впоследствии создадим с помощью конструктора.
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

Показывает, как создавать верхние и нижние колонтитулы в документе с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавляем вместе с ней.
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

// Изменение форматирования применит его к текущей ячейке,
// и любые новые ячейки, которые мы впоследствии создадим с помощью конструктора.
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

Показывает, как построить таблицу с пользовательскими границами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавляем вместе с ней.
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

// Изменение форматирования применит его к текущей ячейке,
// и любые новые ячейки, которые мы впоследствии создадим с помощью конструктора.
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

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
