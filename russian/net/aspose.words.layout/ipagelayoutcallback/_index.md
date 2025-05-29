---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words для .NET
description: Настройте макет документа с помощью интерфейса Aspose.Words.Layout.IPageLayoutCallback. Улучшите рендеринг с помощью собственных методов для достижения оптимальных результатов.
type: docs
weight: 3760
url: /ru/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы ваш собственный метод вызывался во время сборки и рендеринга модели макета страницы.

```csharp
public interface IPageLayoutCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | Вызывается для уведомления о ходе построения макета и рендеринга. |

## Примечания

Основное назначение этого интерфейса — разрешить коду приложения прерывать процесс сборки.

Можно построить модель макета страницы только для нескольких страниц в начале документа, а затем прервать процесс и отобразить только то, что уже построено.

Однако следует отметить, что результаты рендеринга могут не соответствовать результатам рендеринга для каждой страницы, если бы процесс был завершен.

Этот метод может не сработать для каждого документа или вообще не сработать.

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
/// и отображает страницу, которую мы преобразуем в изображение в локальной файловой системе.
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
