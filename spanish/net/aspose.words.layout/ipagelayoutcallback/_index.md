---
title: Interface IPageLayoutCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.IPageLayoutCallback interfaz. Implemente esta interfaz si desea que se llame a su propio método personalizado durante la creación y representación del modelo de diseño de página.
type: docs
weight: 3310
url: /es/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implemente esta interfaz si desea que se llame a su propio método personalizado durante la creación y representación del modelo de diseño de página.

```csharp
public interface IPageLayoutCallback
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(PageLayoutCallbackArgs) | Esto se llama para notificar sobre la construcción del diseño y el progreso de la representación. |

### Observaciones

El uso principal de esta interfaz es permitir que el código de la aplicación cancele el proceso de compilación.

Es posible crear un modelo de diseño de página solo para unas pocas páginas al inicio del documento, luego cancelar el proceso y representar solo lo que ya se ha creado.

Tenga en cuenta, sin embargo, que los resultados de la representación pueden no coincidir con lo que se representaría para cada página si el proceso hubiera finalizado.

Es posible que esta técnica no funcione para todos los documentos o que falle por completo.

### Ejemplos

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

* property [Callback](../layoutoptions/callback/)
* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


