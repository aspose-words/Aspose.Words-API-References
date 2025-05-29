---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words LowCode ComparerContext для эффективного сравнения документов, улучшающего ваш рабочий процесс за счет бесшовной интеграции и мощных функций.
type: docs
weight: 4220
url: /ru/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Средство сравнения документов context

```csharp
public class ComparerContext : ProcessorContext
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ComparerContext](comparercontext/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Указывает, следует ли принимать изменения в документах перед их сравнением. Если сравниваемые документы содержат изменения и этот флаг установлен в значение false, процессор отклонит изменения. Значение по умолчанию:`истинный` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | Автор, который будет назначен редакциям, созданным во время сравнения документов. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Параметры, используемые при сравнении документов. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | Дата и время, назначенные редакциям, созданным во время сравнения документов. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Настройки шрифта, используемые процессором. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Параметры макета документа, используемые процессором. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Предупреждающий обратный вызов, используемый процессором. |

## Примеры

Показывает, как просто сравнивать документы, используя контекст.

```csharp
// Существует несколько способов сравнения документов:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Показывает, как сравнивать документы из потока, используя контекст.

```csharp
// Существует несколько способов сравнения документов из потока:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Смотрите также

* class [ProcessorContext](../processorcontext/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
