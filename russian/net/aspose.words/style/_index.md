---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words для .NET
description: Aspose.Words.Style сорт. Представляет один встроенный или пользовательский стиль на С#.
type: docs
weight: 6130
url: /ru/net/aspose.words/style/
---
## Style class

Представляет один встроенный или пользовательский стиль.

Чтобы узнать больше, посетите[Работа со стилями и темами](https://docs.aspose.com/words/net/working-with-styles-and-themes/) статья документации.

```csharp
public class Style
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Получает все псевдонимы этого стиля. Если стиль не имеет псевдонимов, возвращается пустой массив строк. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Указывает, будет ли этот стиль автоматически переопределяться на основе соответствующего значения. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Получает/устанавливает имя стиля, на котором основан этот стиль. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | True, если этот стиль является одним из встроенных стилей MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | Получает документ владельца. |
| [Font](../../aspose.words/style/font/) { get; } | Получает форматирование символов стиля. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Истинно, если стиль является одним из встроенных стилей заголовков. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Указывает, отображается ли этот стиль в галерее быстрых стилей в пользовательском интерфейсе MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Получает имя`Style` связан с этим. Возвращает пустую строку, если стили не связаны. |
| [List](../../aspose.words/style/list/) { get; } | Получает список, определяющий форматирование этого стиля списка. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Предоставляет доступ к свойствам форматирования списка стиля абзаца. |
| [Name](../../aspose.words/style/name/) { get; set; } | Получает или задает имя стиля. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Получает/устанавливает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца a , отформатированного с использованием указанного стиля. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Получает форматирование абзаца стиля. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Получает независимый от локали идентификатор стиля для встроенного стиля. |
| [Styles](../../aspose.words/style/styles/) { get; } | Получает коллекцию стилей, которым принадлежит этот стиль. |
| [Type](../../aspose.words/style/type/) { get; } | Получает тип стиля (абзац или символ). |

## Методы

| Имя | Описание |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | Сравнивает с указанным стилем. Istd стилей сравниваются только для встроенных стилей. Стили по умолчанию не включаются в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца рекурсивно сравниваются. |
| [Remove](../../aspose.words/style/remove/)() | Удаляет указанный стиль из документа. |

## Примеры

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем собственный стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Примените стиль абзаца к текущему абзацу конструктора документов, а затем добавьте текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль компоновщика документов на стиль без форматирования списка и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Показывает, как создать и применить собственный стиль.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Автоматически переопределить стиль.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Применяем один из стилей документа к абзацу, который создает конструктор документов.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Удаляем наш собственный стиль из коллекции стилей документа.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Любой текст, в котором использовался удаленный стиль, возвращается к форматированию по умолчанию.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
