---
title: PrinterSettingsContainer
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words para .NET
description: Descubra el constructor PrinterSettingsContainer y cree y administre la configuración de su impresora de forma eficiente y sencilla. ¡Optimice su experiencia de impresión hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.rendering/printersettingscontainer/printersettingscontainer/
---
## PrinterSettingsContainer constructor

Crea un contenedor paraPrinterSettings .

```csharp
public PrinterSettingsContainer(PrinterSettings settings)
```

## Ejemplos

Muestra cómo acceder y enumerar las fuentes y tamaños de papel de su impresora.

```csharp
// El "PrinterSettingsContainer" contiene un objeto "PrinterSettings",
// que contiene datos únicos para diferentes controladores de impresora.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// La propiedad "PaperSizes" contiene la lista de tamaños de papel que se deben indicar a la impresora que utilice.
// Tanto PrinterSource como PrinterSize contienen una propiedad "RawKind",
// lo que equivale a un tipo de papel listado en la enumeración PaperSourceKind.
// Si hay una fuente de papel con el mismo valor "RawKind" que el de la página de impresión,
//la impresora imprimirá la página utilizando la fuente y el tamaño de papel proporcionados.
// De lo contrario, la impresora utilizará de manera predeterminada la fuente designada por la propiedad "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Ver también

* class [PrinterSettingsContainer](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
