---
title: DocumentLoadingArgs Class
linktitle: DocumentLoadingArgs
articleTitle: DocumentLoadingArgs
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Loading.DocumentLoadingArgs для эффективной загрузки документов. Улучшите свой рабочий процесс с помощью мощных аргументов уведомлений.
type: docs
weight: 4040
url: /ru/net/aspose.words.loading/documentloadingargs/
---
## DocumentLoadingArgs class

Аргумент передан в[`Notify`](../idocumentloadingcallback/notify/) .

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public sealed class DocumentLoadingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [EstimatedProgress](../../aspose.words.loading/documentloadingargs/estimatedprogress/) { get; } | Общий предполагаемый процент прогресса. |

## Примеры

Показывает, как уведомить пользователя, если загрузка документа превысила ожидаемое время загрузки.

```csharp
public void ProgressCallback()
{
    LoadingProgressCallback progressCallback = new LoadingProgressCallback();

    LoadOptions loadOptions = new LoadOptions { ProgressCallback = progressCallback };

    try
    {
        Document doc = new Document(MyDir + "Big document.docx", loadOptions);
    }
    catch (OperationCanceledException exception)
    {
        Console.WriteLine(exception.Message);

        // Решить проблему длительности загрузки.
    }
}

/// <summary>
/// Отменить загрузку документа по истечении "MaxDuration" секунд.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Ктр.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Метод обратного вызова, вызванный во время загрузки документа.
    /// </summary>
    /// <param name="args">Загрузка аргументов.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Дата и время начала загрузки документа.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Максимально допустимая длительность в сек.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
