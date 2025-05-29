---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Layout.PageLayoutEvent, esencial para optimizar los eventos de diseño de página durante la renderización y creación de documentos. ¡Mejore su flujo de trabajo hoy mismo!
type: docs
weight: 3820
url: /es/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Un código de evento generado durante la creación y representación del modelo de diseño de página.

El modelo de diseño de página se construye en dos pasos. Primero, el "paso de conversión", es cuando el diseño de página extrae el contenido del documento y crea un gráfico de objetos. Segundo, el "paso de reflujo", es cuando las estructuras se dividen, se fusionan y se organizan en páginas.

Dependiendo de la operación que desencadenó la creación, el modelo de diseño de página puede o no representarse en un formato de página fijo. Por ejemplo, calcular el número de páginas del documento o actualizar campos no requiere representación, mientras que exportar a PDF sí.

```csharp
public enum PageLayoutEvent
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Valor predeterminado |
| WatchDog | `1` | Corresponde a un punto de control en el código que se visita con frecuencia y que es adecuado para abortar el proceso. |
| BuildStarted | `2` | Se ha iniciado la creación del diseño de página. Se disparó una vez. Este es el primer evento que ocurre cuando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) se llama. |
| BuildFinished | `3` | La creación del diseño de página ha finalizado. Se disparó una vez. Este es el último evento que ocurre cuando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) se llama. |
| ConversionStarted | `4` | Se ha iniciado la conversión del modelo de documento a diseño de página. Se activó una vez. Esto ocurre cuando el modelo de diseño empieza a extraer el contenido del documento. |
| ConversionFinished | `5` | La conversión del modelo de documento a diseño de página ha finalizado. Se activó una vez. Esto ocurre cuando el modelo de diseño deja de extraer el contenido del documento. |
| ReflowStarted | `6` | Se ha iniciado el reflujo del diseño de página. Se activó una vez. Esto ocurre cuando el modelo de diseño empieza a refluir el contenido del documento. |
| ReflowFinished | `7` | El reflujo del diseño de página ha finalizado. Se activó una vez. Esto ocurre cuando el modelo de diseño deja de refluir el contenido del documento. |
| PartReflowStarted | `8` | El reflujo de la página ha comenzado. Tenga en cuenta que la página puede refluir varias veces y que el reflujo puede reiniciarse antes de finalizar. |
| PartReflowFinished | `9` | El reflujo de la página ha finalizado. Tenga en cuenta que la página puede refluir varias veces y que el reflujo puede reiniciarse antes de finalizar. |
| PartRenderingStarted | `10` | Se ha iniciado la renderización de la página. Se activa una vez por página. |
| PartRenderingFinished | `11` | La renderización de la página ha finalizado. Se activa una vez por página. |

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

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)
