---
title: IDocumentLoadingCallback.Notify
second_title: Referencia de API de Aspose.Words para .NET
description: IDocumentLoadingCallback método. Esto se llama para notificar el progreso de la carga del documento.
type: docs
weight: 10
url: /es/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Esto se llama para notificar el progreso de la carga del documento.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| args | DocumentLoadingArgs | Un argumento del evento. |

### Observaciones

El uso principal de esta interfaz es permitir que el código de la aplicación obtenga el estado de progreso y cancele el proceso de carga.

Se debe generar una excepción desde la devolución de llamada de progreso para el aborto y se debe incluir en el código del consumidor.

### Ejemplos

Muestra cómo notificar al usuario si la carga del documento excedió el tiempo de carga esperado.

```csharp
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

        // Manejar el problema de duración de la carga.
    }
}

/// <summary>
/// Cancelar la carga de un documento después de los segundos de "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Centro.
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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* espacio de nombres [Aspose.Words.Loading](../../idocumentloadingcallback/)
* asamblea [Aspose.Words](../../../)


