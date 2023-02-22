---
title: Interface IDocumentLoadingCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Loading.IDocumentLoadingCallback interfaz. Implemente esta interfaz si desea que se llame a su propio método personalizado durante la carga de un documento.
type: docs
weight: 3430
url: /es/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Implemente esta interfaz si desea que se llame a su propio método personalizado durante la carga de un documento.

```csharp
public interface IDocumentLoadingCallback
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(DocumentLoadingArgs) | Se llama para notificar el progreso de la carga del documento. |

### Ejemplos

Muestra cómo notificar al usuario si la carga del documento excedió el tiempo de carga esperado.

```csharp
[Test]
public void ProgressCallback()
{
    LoadingProgressCallback progressCallback = new LoadingProgressCallback();

    LoadOptions loadOptions = new LoadOptions { ProgressCallback = progressCallback };

    try
    {
        Document doc = new Document(MyDir + "Big document.docx", loadOptions);
    }
    catch (OperationCanceledException exception)
    {
        Console.WriteLine(exception.Message);

        // Manejar el problema de la duración de la carga.
    }
}

/// <summary>
/// Cancelar la carga de un documento después de los segundos "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Centro
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Método de devolución de llamada que llamó durante la carga del documento.
    /// </summary>
    /// <param name="args">Cargando argumentos.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Fecha y hora en que se inicia la carga del documento.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Duración máxima permitida en seg.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)


