---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words para .NET
description: Descubra la propiedad LoadOptions WarningCallback, que le alerta durante las operaciones de carga para evitar la pérdida de datos y garantizar la integridad del formato.
type: docs
weight: 180
url: /es/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Se llama durante una operación de carga, cuando se detecta un problema que podría provocar pérdida de fidelidad de datos o formato.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Ejemplos

Muestra cómo imprimir y almacenar advertencias que ocurren durante la carga de documentos.

```csharp
public void LoadOptionsWarningCallback()
{
    // Cree un nuevo objeto LoadOptions y establezca su atributo WarningCallback
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
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
