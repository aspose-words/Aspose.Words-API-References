---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.IPageLayoutCallback интерфейс. Реализуйте этот интерфейс если вы хотите чтобы во время построения и рендеринга модели макета страницы вызывался собственный метод на С#.
type: docs
weight: 3310
url: /ru/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы во время построения и рендеринга модели макета страницы вызывался собственный метод.

```csharp
public interface IPageLayoutCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | Вызывается для уведомления о построении макета и ходе рендеринга. |

## Примечания

Основное использование этого интерфейса — разрешить коду приложения прерывать процесс сборки.

Можно построить модель макета страницы только для нескольких страниц в начале документа, затем прервать процесс и визуализировать только то, что уже было построено.

Однако обратите внимание, что результаты рендеринга могут не совпадать с тем, что было бы визуализировано для каждой страницы, если бы процесс завершился.

Этот метод может работать не для каждого документа или может оказаться неэффективным.

## Примеры

Показывает, как отслеживать изменения макета с помощью обратного вызова макета.

```csharp
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// Уведомляет нас, когда мы сохраняем документ в фиксированном формате страницы
/// и отображает страницу, на которой мы выполняем перекомпоновку страницы, в изображение в локальной файловой системе.
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### Смотрите также

* property [Callback](../layoutoptions/callback/)
* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
