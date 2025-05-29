---
title: IDocumentLoadingCallback Interface
linktitle: IDocumentLoadingCallback
articleTitle: IDocumentLoadingCallback
second_title: Aspose.Words для .NET
description: Настройте загрузку документов с помощью Aspose.Words.IDocumentLoadingCallback. Реализуйте собственный метод для улучшенного контроля и гибкости в управлении документами.
type: docs
weight: 4080
url: /ru/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы во время загрузки документа вызывался ваш собственный метод.

```csharp
public interface IDocumentLoadingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(*[DocumentLoadingArgs](../documentloadingargs/)*) | Вызывается для уведомления о ходе загрузки документа. |

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
