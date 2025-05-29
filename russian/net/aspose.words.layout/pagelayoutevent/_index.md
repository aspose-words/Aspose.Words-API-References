---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Layout.PageLayoutEvent — необходимое для оптимизации событий макета страницы во время рендеринга и построения документа. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 3820
url: /ru/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Код события, возникающего во время построения и рендеринга модели макета страницы.

Модель макета страницы строится в два этапа. Первый, «этап преобразования», на котором макет страницы извлекает содержимое документа и создает граф объектов. Второй, «этап переформатирования», на котором структуры разделяются, объединяются и организуются в страницы.

В зависимости от операции, запустившей сборку, модель макета страницы может быть или не быть дополнительно преобразована в фиксированный формат страницы. Например, вычисление количества страниц в документе или обновление полей не требует преобразования, тогда как экспорт в PDF требует.

```csharp
public enum PageLayoutEvent
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Значение по умолчанию |
| WatchDog | `1` | Соответствует контрольной точке в коде, которая часто посещается и подходит для прерывания процесса. |
| BuildStarted | `2` | Началась сборка макета страницы. Срабатывает один раз. Это первое событие, которое происходит, когда[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) называется . |
| BuildFinished | `3` | Сборка макета страницы завершена. Срабатывает один раз. Это последнее событие, которое происходит, когда[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) называется . |
| ConversionStarted | `4` | Начато преобразование модели документа в макет страницы. Срабатывает один раз. Это происходит, когда модель макета начинает извлекать содержимое документа. |
| ConversionFinished | `5` | Преобразование модели документа в макет страницы завершено. Срабатывает один раз. Это происходит, когда модель макета прекращает извлекать содержимое документа. |
| ReflowStarted | `6` | Переформатирование макета страницы началось. Срабатывает один раз. Это происходит, когда модель макета начинает переформатирование содержимого документа. |
| ReflowFinished | `7` | Переформатирование макета страницы завершено. Срабатывает один раз. Это происходит, когда модель макета прекращает переформатирование содержимого документа. |
| PartReflowStarted | `8` | Переформатирование страницы началось. Обратите внимание, что страница может переформатироваться несколько раз и что переформатирование может возобновиться до его завершения. |
| PartReflowFinished | `9` | Переформатирование страницы завершено. Обратите внимание, что страница может переформатироваться несколько раз и что переформатирование может возобновиться до завершения. |
| PartRenderingStarted | `10` | Рендеринг страницы начался. Это происходит один раз на страницу. |
| PartRenderingFinished | `11` | Рендеринг страницы завершен. Это происходит один раз на страницу. |

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
