---
title: TableStyle Class
linktitle: TableStyle
articleTitle: TableStyle
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.TableStyle для создания и настройки потрясающих стилей таблиц в ваших документах. Улучшите форматирование без усилий!
type: docs
weight: 7070
url: /ru/net/aspose.words/tablestyle/
---
## TableStyle class

Представляет стиль таблицы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) документальная статья.

```csharp
public class TableStyle : Style
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Получает все псевдонимы этого стиля. Если у стиля нет псевдонимов, то возвращается пустой массив строк. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Задает выравнивание для стиля таблицы. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Возвращает или задает флаг, указывающий, разрешено ли разделять текст в строке таблицы через разрыв страницы. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Указывает, будет ли этот стиль автоматически переопределяться на основе соответствующего значения. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Получает/задает имя стиля, на котором основан этот стиль. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Возвращает или задает, является ли это стилем для таблицы с направлением справа налево. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Получает коллекцию границ ячеек по умолчанию для стиля. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого под содержимым ячеек таблицы. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Истина, если этот стиль является одним из встроенных стилей в MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Возвращает или задает величину пространства (в пунктах) между ячейками. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Возвращает или задает количество столбцов, включаемых в полосу, когда стиль задает полосу четных/нечетных столбцов. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Коллекция условных стилей, которые могут быть определены для этого стиля таблицы. |
| [Document](../../aspose.words/style/document/) { get; } | Получает документ владельца. |
| [Font](../../aspose.words/style/font/) { get; } | Получает форматирование символов стиля. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Истинно, когда стиль является одним из встроенных стилей заголовков. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Указывает, отображается ли этот стиль в галерее быстрых стилей в пользовательском интерфейсе MS Word. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Возвращает или задает значение, представляющее левый отступ таблицы. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого слева от содержимого ячеек таблицы. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; set; } | Получает/устанавливает имя[`Style`](../style/) связан с этим. Возвращает пустую строку, если ни один стиль не связан. |
| [List](../../aspose.words/style/list/) { get; } | Получает список, определяющий форматирование этого стиля списка. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Предоставляет доступ к свойствам форматирования списка стиля абзаца. |
| [Locked](../../aspose.words/style/locked/) { get; set; } | Указывает, заблокирован ли этот стиль. |
| [Name](../../aspose.words/style/name/) { get; set; } | Получает или задает имя стиля. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Возвращает/задает имя стиля, который будет автоматически применен к новому абзацу, вставленному после абзаца a , отформатированного с использованием указанного стиля. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Получает форматирование абзаца стиля. |
| [Priority](../../aspose.words/style/priority/) { get; set; } | Возвращает/задает целочисленное значение, представляющее приоритет сортировки стилей на панели задач «Стили». |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого справа от содержимого ячеек таблицы. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Возвращает или задает количество строк, включаемых в полосу, когда стиль задает полосу четных/нечетных строк. |
| [SemiHidden](../../aspose.words/style/semihidden/) { get; set; } | Возвращает/задает, будет ли стиль скрыт из галереи стилей и из панели задач «Стили». |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Получает[`Shading`](../shading/) объект, который ссылается на форматирование затенения ячеек таблицы. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Получает независимый от локали идентификатор стиля для встроенного стиля. |
| [Styles](../../aspose.words/style/styles/) { get; } | Получает коллекцию стилей, к которой принадлежит этот стиль. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого над содержимым ячеек таблицы. |
| [Type](../../aspose.words/style/type/) { get; } | Получает тип стиля (абзац или символ). |
| [UnhideWhenUsed](../../aspose.words/style/unhidewhenused/) { get; set; } | Возвращает/задает, отображается ли стиль, используемый в текущем документе, из галереи стилей и из панели задач «Стили». True, когда используемый стиль должен отображаться в галерее стилей. |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Задает вертикальное выравнивание ячеек. |

## Методы

| Имя | Описание |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(*[Style](../style/)*) | Сравнивает с указанным стилем. Сравниваются только стили Istds для встроенных стилей. Стили по умолчанию не включаются в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца сравниваются рекурсивно. |
| [Remove](../../aspose.words/style/remove/)() | Удаляет указанный стиль из документа. |

## Примеры

Показывает, как создать пользовательские настройки стиля для таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Установка свойств стиля таблицы может повлиять на свойства самой таблицы.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Смотрите также

* class [Style](../style/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
