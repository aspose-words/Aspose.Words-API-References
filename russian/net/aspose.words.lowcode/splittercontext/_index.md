---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.LowCode.SplitterContext для эффективного разделения документов, улучшающего ваш рабочий процесс за счет бесшовной интеграции и мощной функциональности.
type: docs
weight: 4430
url: /ru/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Контекст разделителя документов.

```csharp
public class SplitterContext : ProcessorContext
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [SplitterContext](splittercontext/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Настройки шрифта, используемые процессором. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Параметры макета документа, используемые процессором. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Параметры разделения документа. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Предупреждающий обратный вызов, используемый процессором. |

## Примеры

Показывает, как разделить документ по страницам, используя контекст.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Показывает, как разделить документ из потока по страницам, используя контекст.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### Смотрите также

* class [ProcessorContext](../processorcontext/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
