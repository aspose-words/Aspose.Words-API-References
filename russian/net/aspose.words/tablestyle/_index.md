---
title: TableStyle Class
linktitle: TableStyle
articleTitle: TableStyle
second_title: Aspose.Words для .NET
description: Aspose.Words.TableStyle сорт. Представляет стиль таблицы на С#.
type: docs
weight: 6220
url: /ru/net/aspose.words/tablestyle/
---
## TableStyle class

Представляет стиль таблицы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) статья документации.

```csharp
public class TableStyle : Style
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Получает все псевдонимы этого стиля. Если стиль не имеет псевдонимов, возвращается пустой массив строк. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Определяет выравнивание стиля таблицы. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Получает или задает флаг, указывающий, разрешено ли разделение текста в строке таблицы по разрыву страницы. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Указывает, будет ли этот стиль автоматически переопределяться на основе соответствующего значения. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Получает/устанавливает имя стиля, на котором основан этот стиль. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Получает или задает, является ли это стилем для таблицы с письмом справа налево. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Получает коллекцию границ ячеек по умолчанию для стиля. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Получает или задает объем пространства (в пунктах), добавляемого под содержимым ячеек таблицы. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | True, если этот стиль является одним из встроенных стилей MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Получает или задает расстояние (в пунктах) между ячейками. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Получает или задает количество столбцов, которые необходимо включить в группировку, когда стиль определяет группировку нечетных/четных столбцов. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Коллекция условных стилей, которые могут быть определены для этого стиля таблицы. |
| [Document](../../aspose.words/style/document/) { get; } | Получает документ владельца. |
| [Font](../../aspose.words/style/font/) { get; } | Получает форматирование символов стиля. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Истинно, если стиль является одним из встроенных стилей заголовков. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Указывает, отображается ли этот стиль в галерее быстрых стилей в пользовательском интерфейсе MS Word. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Получает или задает значение, представляющее левый отступ таблицы. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Получает или задает объем места (в пунктах), добавляемый слева от содержимого ячеек таблицы. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Получает имя[`Style`](../style/) связан с этим. Возвращает пустую строку, если стили не связаны. |
| [List](../../aspose.words/style/list/) { get; } | Получает список, определяющий форматирование этого стиля списка. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Предоставляет доступ к свойствам форматирования списка стиля абзаца. |
| [Name](../../aspose.words/style/name/) { get; set; } | Получает или задает имя стиля. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Получает/устанавливает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца a , отформатированного с использованием указанного стиля. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Получает форматирование абзаца стиля. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Получает или задает объем места (в пунктах), добавляемый справа от содержимого ячеек таблицы. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Получает или задает количество строк, которые необходимо включить в группировку, когда стиль определяет нечетную/четную группировку строк. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Получает[`Shading`](../shading/) объект, который относится к форматированию затенения ячеек таблицы. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Получает независимый от локали идентификатор стиля для встроенного стиля. |
| [Styles](../../aspose.words/style/styles/) { get; } | Получает коллекцию стилей, которым принадлежит этот стиль. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Получает или задает объем пространства (в пунктах), добавляемого над содержимым ячеек таблицы. |
| [Type](../../aspose.words/style/type/) { get; } | Получает тип стиля (абзац или символ). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Определяет вертикальное выравнивание ячеек. |

## Методы

| Имя | Описание |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(*[Style](../style/)*) | Сравнивает с указанным стилем. Istd стилей сравниваются только для встроенных стилей. Стили по умолчанию не включаются в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца рекурсивно сравниваются. |
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
