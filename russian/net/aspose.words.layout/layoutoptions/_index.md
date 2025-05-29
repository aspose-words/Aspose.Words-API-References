---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Layout.LayoutOptions для оптимизации управления макетом документа, расширяя возможности обработки Word с помощью гибких параметров настройки.
type: docs
weight: 3800
url: /ru/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Содержит параметры, позволяющие управлять процессом макетирования документа.

Чтобы узнать больше, посетите[Преобразование в формат с фиксированным размером страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) документальная статья.

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
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Возвращает или задает способ отображения комментариев. Значение по умолчанию:ShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Возвращает или задает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Возвращает или задает указание того, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». Значение по умолчанию:`истинный` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Возвращает или задает указание того, следует ли использовать исходные метрики шрифта после замены шрифта. Значение по умолчанию:`истинный` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Получает параметры ревизии. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Возвращает или задает признак того, отображается ли скрытый текст в документе. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Возвращает или задает указание того, отображаются ли знаки абзаца. Значение по умолчанию:`ЛОЖЬ` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Получает или устанавливает[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) реализация, используемая для функций рендеринга расширенной типографики. |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Используйте[`LayoutOptions`](../../aspose.words/document/layoutoptions/) свойство для доступа к параметрам макета для этого документа.

Обратите внимание, что после изменения любого из параметров, присутствующих в этом классе,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Для применения измененных параметров к макету необходимо вызвать method .

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

Показывает, как отображать знаки абзацев в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавьте несколько абзацев, затем включите знаки абзацев, чтобы отображать концы абзацев
// с символом "¶" при рендеринге документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Показывает, как изменить внешний вид изменений в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
