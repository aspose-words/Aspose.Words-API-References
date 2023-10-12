---
title: LoadOptions.WarningCallback
second_title: Referencia de API de Aspose.Words para .NET
description: LoadOptions propiedad. Se llama durante una operación de carga cuando se detecta un problema que podría provocar la pérdida de fidelidad de los datos o del formato.
type: docs
weight: 170
url: /es/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Se llama durante una operación de carga, cuando se detecta un problema que podría provocar la pérdida de fidelidad de los datos o del formato.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Ejemplos

Muestra cómo imprimir y almacenar advertencias que ocurren durante la carga de documentos.

```csharp
public void LoadOptionsWarningCallback()
{
    // Crea un nuevo objeto LoadOptions y establece su atributo AdvertenciaCallback
    // como una instancia de nuestra implementación IWarningCallback.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Nuestra devolución de llamada imprimirá todas las advertencias que surjan durante la operación de carga.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback que imprime advertencias y sus detalles a medida que surgen durante la carga del documento.
/// </summary>
private class DocumentLoadingWarningCallback : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        Console.WriteLine($"Warning: {info.WarningType}");
        Console.WriteLine($"\tSource: {info.Source}");
        Console.WriteLine($"\tDescription: {info.Description}");
        mWarnings.Add(info);
    }

    public List<WarningInfo> GetWarnings()
    {
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Ver también

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)


