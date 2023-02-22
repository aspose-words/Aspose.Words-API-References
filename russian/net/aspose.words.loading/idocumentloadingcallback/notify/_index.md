---
title: IDocumentLoadingCallback.Notify
second_title: Справочник по API Aspose.Words для .NET
description: IDocumentLoadingCallback метод. Вызывается для уведомления о ходе загрузки документа.
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

### Примечания

Основное использование этого интерфейса — разрешить коду приложения получать статус выполнения и прерывать процесс загрузки.

Исключение должно быть выброшено из обратного вызова прогресса для аборта и должно быть перехвачено в коде потребителя.

### Примеры

Показывает, как уведомить пользователя, если загрузка документа превысила ожидаемое время загрузки.

```csharp
[Test]
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

        // Обработка проблемы продолжительности загрузки.
    }
}

/// <summary>
/// Отменить загрузку документа по истечении "MaxDuration" секунд.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Контр.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Метод обратного вызова, который вызывается при загрузке документа.
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
    /// Максимально допустимая продолжительность в сек.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Смотрите также

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* пространство имен [Aspose.Words.Loading](../../idocumentloadingcallback/)
* сборка [Aspose.Words](../../../)


