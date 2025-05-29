---
title: PageLayoutCallbackArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageLayoutCallbackArgs Document для эффективного доступа и управления данными документа. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.layout/pagelayoutcallbackargs/document/
---
## PageLayoutCallbackArgs.Document property

Получает документ.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [PageLayoutCallbackArgs](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
