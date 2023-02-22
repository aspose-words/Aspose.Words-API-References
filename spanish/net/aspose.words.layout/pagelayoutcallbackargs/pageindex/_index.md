---
title: PageLayoutCallbackArgs.PageIndex
second_title: Referencia de API de Aspose.Words para .NET
description: PageLayoutCallbackArgs propiedad. Obtiene el índice basado en 0 de la página en el documento al que se relaciona este evento. Devuelve un valor negativo si no hay una página asociada o si la página se eliminó durante el reflujo.
type: docs
weight: 30
url: /es/net/aspose.words.layout/pagelayoutcallbackargs/pageindex/
---
## PageLayoutCallbackArgs.PageIndex property

Obtiene el índice basado en 0 de la página en el documento al que se relaciona este evento. Devuelve un valor negativo si no hay una página asociada o si la página se eliminó durante el reflujo.

```csharp
public int PageIndex { get; }
```

### Ejemplos

Muestra cómo realizar un seguimiento de los cambios de diseño con una devolución de llamada de diseño.

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
/// Nos notifica cuando guardamos el documento en un formato de página fijo
/// y representa una página en la que realizamos un reflujo de página en una imagen en el sistema de archivos local.
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

### Ver también

* class [PageLayoutCallbackArgs](../)
* espacio de nombres [Aspose.Words.Layout](../../pagelayoutcallbackargs/)
* asamblea [Aspose.Words](../../../)


