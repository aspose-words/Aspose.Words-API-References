---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.LayoutOptions сорт. Содержит параметры позволяющие управлять процессом макетирования документа на С#.
type: docs
weight: 3350
url: /ru/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Содержит параметры, позволяющие управлять процессом макетирования документа.

Чтобы узнать больше, посетите[Преобразование в формат фиксированной страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) статья документации.

```csharp
public class LayoutOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Получает или устанавливает[`IPageLayoutCallback`](../ipagelayoutcallback/) реализация, используемая моделью макета страницы. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Получает или задает способ отображения комментариев. Значение по умолчанию:ShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Получает или задает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Получает или задает индикатор того, игнорируется ли параметр совместимости «Использовать метрики принтера для макета документа». Значение по умолчанию —`истинный` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Получает или задает указание того, следует ли использовать исходные метрики шрифта после замены шрифта. Значение по умолчанию:`истинный` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Получает параметры версии. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Получает или задает индикатор того, отображается ли скрытый текст в документе. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Получает или задает индикатор того, отображаются ли знаки абзаца. Значение по умолчанию:`ЛОЖЬ` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Получает или устанавливает[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) реализация, используемая для функций рендеринга расширенной типографики. |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Использовать[`LayoutOptions`](../../aspose.words/document/layoutoptions/) свойство для доступа к параметрам макета для этого документа.

Обратите внимание, что после изменения любого из параметров, присутствующих в этом классе,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Метод следует вызывать, чтобы измененные параметры были применены к макету.

## Примеры

Показывает, как скрыть текст в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Вставляем скрытый текст, затем указываем, хотим ли мы исключить его из отображаемого документа.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Показывает, как отображать знаки абзаца в готовом к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавляем несколько абзацев, затем включаем знаки абзацев, чтобы показывать концы абзацев
// с символом подставки (¶) при рендеринге документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Показывает, как изменить внешний вид редакций в готовом к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем ревизию, затем меняем цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
