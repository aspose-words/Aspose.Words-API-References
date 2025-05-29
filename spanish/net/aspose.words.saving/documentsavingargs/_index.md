---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.DocumentSavingArgs, esencial para gestionar eventos de guardado de documentos de manera eficiente en sus aplicaciones.
type: docs
weight: 5700
url: /es/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Un argumento pasado a[`Notify`](../idocumentsavingcallback/notify/) .

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) Artículo de documentación.

```csharp
public sealed class DocumentSavingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Porcentaje de progreso estimado general. |

## Ejemplos

Muestra cómo administrar un documento mientras se guarda en html.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    //Se admiten los siguientes formatos: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Retrollamada de progreso de guardado. Cancelar el guardado del documento después de los segundos de "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Método de devolución de llamada que se llamó durante el guardado del documento.
    /// </summary>
    /// <param name="args">Guardando argumentos.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Fecha y hora en que se inicia el guardado del documento.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Duración máxima permitida en segundos.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
