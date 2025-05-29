---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Style для управления пользовательскими и встроенными стилями без усилий. Улучшите форматирование документов с легкостью и точностью.
type: docs
weight: 6980
url: /ru/net/aspose.words/style/
---
## Style class

Представляет один встроенный или определенный пользователем стиль.

Чтобы узнать больше, посетите[Работа со стилями и темами](https://docs.aspose.com/words/net/working-with-styles-and-themes/) документальная статья.

```csharp
public class Style
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Получает все псевдонимы этого стиля. Если у стиля нет псевдонимов, то возвращается пустой массив строк. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Указывает, будет ли этот стиль автоматически переопределяться на основе соответствующего значения. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Получает/задает имя стиля, на котором основан этот стиль. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Истина, если этот стиль является одним из встроенных стилей в MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | Получает документ владельца. |
| [Font](../../aspose.words/style/font/) { get; } | Получает форматирование символов стиля. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Истинно, когда стиль является одним из встроенных стилей заголовков. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Указывает, отображается ли этот стиль в галерее быстрых стилей в пользовательском интерфейсе MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; set; } | Получает/устанавливает имя`Style` связан с этим. Возвращает пустую строку, если ни один стиль не связан. |
| [List](../../aspose.words/style/list/) { get; } | Получает список, определяющий форматирование этого стиля списка. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Предоставляет доступ к свойствам форматирования списка стиля абзаца. |
| [Locked](../../aspose.words/style/locked/) { get; set; } | Указывает, заблокирован ли этот стиль. |
| [Name](../../aspose.words/style/name/) { get; set; } | Получает или задает имя стиля. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Возвращает/задает имя стиля, который будет автоматически применен к новому абзацу, вставленному после абзаца a , отформатированного с использованием указанного стиля. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Получает форматирование абзаца стиля. |
| [Priority](../../aspose.words/style/priority/) { get; set; } | Возвращает/задает целочисленное значение, представляющее приоритет сортировки стилей на панели задач «Стили». |
| [SemiHidden](../../aspose.words/style/semihidden/) { get; set; } | Возвращает/задает, будет ли стиль скрыт из галереи стилей и из панели задач «Стили». |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Получает независимый от локали идентификатор стиля для встроенного стиля. |
| [Styles](../../aspose.words/style/styles/) { get; } | Получает коллекцию стилей, к которой принадлежит этот стиль. |
| [Type](../../aspose.words/style/type/) { get; } | Получает тип стиля (абзац или символ). |
| [UnhideWhenUsed](../../aspose.words/style/unhidewhenused/) { get; set; } | Возвращает/задает, отображается ли стиль, используемый в текущем документе, из галереи стилей и из панели задач «Стили». True, когда используемый стиль должен отображаться в галерее стилей. |

## Методы

| Имя | Описание |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | Сравнивает с указанным стилем. Сравниваются только стили Istds для встроенных стилей. Стили по умолчанию не включаются в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца сравниваются рекурсивно. |
| [Remove](../../aspose.words/style/remove/)() | Удаляет указанный стиль из документа. |

## Примеры

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать пользовательский стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Применяем стиль абзаца к текущему абзацу конструктора документа, а затем добавляем текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль конструктора документов на такой, который не имеет форматирования списка, и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Показывает, как создать и применить пользовательский стиль.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Автоматически переопределить стиль.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Применить один из стилей документа к абзацу, создаваемому конструктором документа.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Удаляем наш пользовательский стиль из коллекции стилей документа.
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
