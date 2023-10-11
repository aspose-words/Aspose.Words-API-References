---
title: Interface IDocumentSavingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.IDocumentSavingCallback интерфейс. Реализуйте этот интерфейс если вы хотите чтобы во время сохранения документа вызывался собственный метод.
type: docs
weight: 5150
url: /ru/net/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы во время сохранения документа вызывался собственный метод.

```csharp
public interface IDocumentSavingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [Notify](../../aspose.words.saving/idocumentsavingcallback/notify/)(DocumentSavingArgs) | Вызывается для уведомления о ходе сохранения документа. |

### Примеры

Показывает, как управлять документом при сохранении в HTML.

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
/// Сохранение обратного вызова прогресса. Отменить сохранение документа по истечении секунд «MaxDuration».
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Центр.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Метод обратного вызова, который вызывается при сохранении документа.
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
    /// Максимально допустимая продолжительность в секундах.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Показывает, как управлять документом при сохранении в docx.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Поддерживаются следующие форматы: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Сохранение обратного вызова прогресса. Отменить сохранение документа по истечении секунд «MaxDuration».
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Центр.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Метод обратного вызова, который вызывается при сохранении документа.
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
    /// Максимально допустимая продолжительность в секундах.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Показывает, как управлять документом при сохранении в xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Поддерживаются следующие форматы: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Сохранение обратного вызова прогресса. Отменить сохранение документа по истечении секунд «MaxDuration».
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Центр.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Метод обратного вызова, который вызывается при сохранении документа.
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
    /// Максимально допустимая продолжительность в секундах.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


