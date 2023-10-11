---
title: Enum PageLayoutEvent
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.PageLayoutEvent enumeración. Un código de evento generado durante la creación y representación del modelo de diseño de página.
type: docs
weight: 3370
url: /es/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Un código de evento generado durante la creación y representación del modelo de diseño de página.

El modelo de diseño de página se construye en dos pasos. Primero, "paso de conversión", aquí es cuando el diseño de página extrae el contenido del documento y crea un gráfico de objetos. Segundo, "paso de reflujo", aquí es cuando las estructuras se dividen, fusionan y organizan en páginas.

Dependiendo de la operación que desencadenó la compilación, el modelo de diseño de página puede o no representarse en un formato de página fijo. Por ejemplo, calcular el número de páginas en el documento o actualizar campos no requiere renderizado, mientras que exportar a PDF sí.

```csharp
public enum PageLayoutEvent
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Valor predeterminado |
| WatchDog | `1` | Corresponde a un punto de control en el código que se visita con frecuencia y que es adecuado para abortar el proceso. |
| BuildStarted | `2` | Se ha iniciado la creación del diseño de página. Disparado una vez. Este es el primer evento que ocurre cuando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) se llama. |
| BuildFinished | `3` | La construcción del diseño de página ha finalizado. Disparado una vez. Este es el último evento que ocurre cuando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) se llama. |
| ConversionStarted | `4` | Se ha iniciado la conversión del modelo de documento al diseño de página. Se disparó una vez. Esto ocurre cuando el modelo de diseño comienza a extraer el contenido del documento. |
| ConversionFinished | `5` | La conversión del modelo de documento al diseño de página ha finalizado. Se disparó una vez. Esto ocurre cuando el modelo de diseño deja de extraer el contenido del documento. |
| ReflowStarted | `6` | Se ha iniciado el reflujo del diseño de página. Se disparó una vez. Esto ocurre cuando el modelo de diseño comienza a redistribuir el contenido del documento. |
| ReflowFinished | `7` | El reflujo del diseño de página ha finalizado. Se disparó una vez. Esto ocurre cuando el modelo de diseño deja de distribuir el contenido del documento. |
| PartReflowStarted | `8` | El reflujo de la página ha comenzado. Tenga en cuenta que la página puede refluir varias veces y que el reflujo puede reiniciarse antes de finalizar. |
| PartReflowFinished | `9` | El reflujo de la página ha finalizado. Tenga en cuenta que la página puede refluir varias veces y que el reflujo puede reiniciarse antes de finalizar. |
| PartRenderingStarted | `10` | Se ha iniciado el procesamiento de la página. Esto se activa una vez por página. |
| PartRenderingFinished | `11` | La renderización de la página ha finalizado. Esto se activa una vez por página. |

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

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


