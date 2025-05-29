---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words для .NET
description: Отслеживайте ход загрузки документа без усилий с помощью метода IDocumentLoadingCallback Notify. Улучшите пользовательский опыт с помощью обновлений в реальном времени!
type: docs
weight: 10
url: /ru/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Вызывается для уведомления о ходе загрузки документа.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | DocumentLoadingArgs | Аргумент события. |

## Примечания

Основное применение этого интерфейса — позволить коду приложения получать статус выполнения и прерывать процесс загрузки.

Исключение должно быть выдано из обратного вызова прогресса для аборта и перехвачено в коде потребителя.

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
