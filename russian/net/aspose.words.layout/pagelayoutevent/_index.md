---
title: PageLayoutEvent
second_title: Справочник по API Aspose.Words для .NET
description: Код события возникшего во время построения и рендеринга модели макета страницы.
type: docs
weight: 3120
url: /ru/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Код события, возникшего во время построения и рендеринга модели макета страницы.

Модель макета страницы строится в два этапа. Во-первых, "этап преобразования", когда макет страницы извлекает содержимое документа и создает граф объектов. Во-вторых, "шаг перекомпоновки", когда структуры разделяются, объединяются и располагаются на страницах.

В зависимости от операции, вызвавшей сборку, модель компоновки страницы может или не может быть дополнительно преобразована в фиксированный формат страницы. Например, вычисление количества страниц в документе или обновление полей не требует рендеринга, тогда как экспорт в Pdf требует.

```csharp
public enum PageLayoutEvent
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Значение по умолчанию |
| WatchDog | `1` | Соответствует часто посещаемой контрольной точке в коде, которая подходит для прерывания процесса. |
| BuildStarted | `2` | Начата сборка макета страницы. Выстрелил один раз. Это первое событие, которое происходит при вызове[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout). |
| BuildFinished | `3` | Сборка макета страницы завершена. Выстрелил один раз. Это последнее событие, которое происходит при вызове[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout). |
| ConversionStarted | `4` | Начато преобразование модели документа в макет страницы. Выстрелил один раз. Это происходит, когда модель макета начинает извлекать содержимое документа. |
| ConversionFinished | `5` | Преобразование модели документа в макет страницы завершено. Выстрелил один раз. Это происходит, когда модель макета перестает извлекать содержимое документа. |
| ReflowStarted | `6` | Начата перекомпоновка макета страницы. Выстрелил один раз. Это происходит, когда модель макета начинает переформатировать содержимое документа. |
| ReflowFinished | `7` | Перекомпоновка макета страницы завершена. Выстрелил один раз. Это происходит, когда модель макета перестает переформатировать содержимое документа. |
| PartReflowStarted | `8` | Началась перекомпоновка страницы. Обратите внимание, что страница может переформатироваться несколько раз, и эта перекомпоновка может перезапуститься до того, как она будет завершена. |
| PartReflowFinished | `9` | Перекомпоновка страницы завершена. Обратите внимание, что страница может переформатироваться несколько раз, и эта перекомпоновка может перезапуститься до того, как она будет завершена. |
| PartRenderingStarted | `10` | Рендеринг страницы начался. Это запускается один раз на странице. |
| PartRenderingFinished | `11` | Рендеринг страницы завершен. Это запускается один раз на странице. |

### Примеры

Показывает, как отслеживать изменения макета с помощью обратного вызова макета.

```csharp
[Test]
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
 /// Уведомляет нас, когда мы сохраняем документ на фиксированную страницу format
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

* namespace [Aspose.Words.Layout](../../aspose.words.layout)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
