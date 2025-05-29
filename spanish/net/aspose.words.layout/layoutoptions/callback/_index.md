---
title: LayoutOptions.Callback
linktitle: Callback
articleTitle: Callback
second_title: Aspose.Words para .NET
description: Descubra la propiedad de devolución de llamada LayoutOptions para administrar fácilmente IPageLayoutCallback para una mejor personalización del diseño de página y una mejor experiencia del usuario.
type: docs
weight: 20
url: /es/net/aspose.words.layout/layoutoptions/callback/
---
## LayoutOptions.Callback property

Obtiene o establece[`IPageLayoutCallback`](../../ipagelayoutcallback/) Implementación utilizada por el modelo de diseño de página.

```csharp
public IPageLayoutCallback Callback { get; set; }
```

## Ejemplos

Muestra cómo realizar un seguimiento de los cambios de diseño con una devolución de llamada de diseño.

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
/// Nos avisa cuando guardamos el documento en un formato de página fijo
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

* interface [IPageLayoutCallback](../../ipagelayoutcallback/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
