---
title: Class LayoutOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Layout.LayoutOptions сорт. Содержит параметры позволяющие управлять процессом компоновки документа.
type: docs
weight: 3150
url: /ru/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Содержит параметры, позволяющие управлять процессом компоновки документа.

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
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Получает или устанавливает[`IPageLayoutCallback`](../ipagelayoutcallback/)реализация, используемая моделью макета страницы. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Получает или задает способ отображения комментариев. Значение по умолчанию:ShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Получает или задает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Получает или задает индикацию того, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». Значение по умолчанию — True. |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Получает параметры версии. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Получает или задает индикацию того, визуализируется ли скрытый текст в документе. Значение по умолчанию — False. |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Получает или задает индикацию того, отображаются ли знаки абзаца. Значение по умолчанию — False. |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Получает или устанавливает[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) реализация, используемая для функций рендеринга Advanced Typography. |

### Примечания

Вы не создаете экземпляры этого класса напрямую. Использовать[`LayoutOptions`](../../aspose.words/document/layoutoptions/)для доступа к параметрам макета для этого документа.

Обратите внимание, что после изменения любого из параметров, присутствующих в этом классе,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) method должен быть вызван для того, чтобы измененные параметры были применены к макету.

### Примеры

Показывает, как скрыть текст в визуализируемом выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Вставляем скрытый текст, затем указываем, хотим ли мы исключить его из визуализируемого документа.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Показывает, как отображать метки абзаца в визуализируемом выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавьте несколько абзацев, затем включите метки абзаца, чтобы показать концы абзацев
// с символом пилкроу (¶) при отображении документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Показывает, как изменить внешний вид редакций в подготовленном к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удаляем полосу, которая появляется слева от каждой исправленной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)


