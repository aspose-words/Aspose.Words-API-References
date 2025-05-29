---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.DocumentSavingArgs, необходимый для эффективной обработки событий сохранения документов в ваших приложениях.
type: docs
weight: 5700
url: /ru/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Аргумент передан в[`Notify`](../idocumentsavingcallback/notify/) .

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public sealed class DocumentSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Общий предполагаемый процент прогресса. |

## Примеры

Показывает, как управлять документом при сохранении в формате HTML.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Поддерживаются следующие форматы: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Обратный вызов хода сохранения. Отменить сохранение документа после "MaxDuration" секунд.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ктр.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Метод обратного вызова, вызываемый во время сохранения документа.
    /// </summary>
    /// <param name="args">Сохранение аргументов.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Дата и время начала сохранения документа.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Максимально допустимая длительность в сек.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
