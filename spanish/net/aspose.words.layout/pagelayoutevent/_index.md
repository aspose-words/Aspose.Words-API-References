---
title: PageLayoutEvent
second_title: Referencia de API de Aspose.Words para .NET
description: Un código de evento generado durante la generación y representación del modelo de diseño de página.
type: docs
weight: 3170
url: /es/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Un código de evento generado durante la generación y representación del modelo de diseño de página.

El modelo de diseño de página se crea en dos pasos. Primero, "paso de conversión", esto es cuando el diseño de página extrae el contenido del documento y crea un gráfico de objetos. Segundo, "paso de reflujo", esto es cuando las estructuras se dividen, fusionan y organizan en páginas.

Dependiendo de la operación que desencadenó la construcción, el modelo de diseño de página puede o no convertirse en un formato de página fijo.

```csharp
public enum PageLayoutEvent
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Valor predeterminado |
| WatchDog | `1` | Corresponde a un punto de control en el código que se visita con frecuencia y que es adecuado para abortar el proceso. |
| BuildStarted | `2` | Se ha iniciado la creación del diseño de página. Disparado una vez. Este es el primer evento que ocurre cuando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout) se llama. |
| BuildFinished | `3` | Ha finalizado la compilación del diseño de página. Disparado una vez. Este es el último evento que ocurre cuando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout) se llama. |
| ConversionStarted | `4` | Se ha iniciado la conversión del modelo de documento al diseño de página. Activado una vez. Esto ocurre cuando el modelo de diseño comienza a extraer contenido del documento. |
| ConversionFinished | `5` | Ha finalizado la conversión del modelo de documento al diseño de página. Activado una vez. Esto ocurre cuando el modelo de diseño deja de extraer contenido del documento. |
| ReflowStarted | `6` | Se ha iniciado el reflujo del diseño de página. Activado una vez. Esto ocurre cuando el modelo de diseño comienza a redistribuir el contenido del documento. |
| ReflowFinished | `7` | Ha finalizado el reflujo del diseño de página. Activado una vez. Esto ocurre cuando el modelo de diseño deja de redistribuir el contenido del documento. |
| PartReflowStarted | `8` | Se ha iniciado el reflujo de la página. Tenga en cuenta que la página puede redistribuirse varias veces y que el reflujo puede reiniciarse antes de que finalice. |
| PartReflowFinished | `9` | El reflujo de la página ha finalizado. Tenga en cuenta que la página puede redistribuirse varias veces y que el reflujo puede reiniciarse antes de que finalice. |
| PartRenderingStarted | `10` | Se ha iniciado el procesamiento de la página. Esto se activa una vez por página. |
| PartRenderingFinished | `11` | Ha finalizado el renderizado de la página. Esto se activa una vez por página. |

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

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
