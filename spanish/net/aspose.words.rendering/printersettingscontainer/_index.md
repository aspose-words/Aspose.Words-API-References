---
title: Class PrinterSettingsContainer
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Rendering.PrinterSettingsContainer clase. Representa un almacenamiento para algunos parámetros dePrinterSettings objeto.
type: docs
weight: 4580
url: /es/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Representa un almacenamiento para algunos parámetros dePrinterSettings objeto.

Para obtener más información, visite el[Imprimir un documento mediante programación o mediante cuadros de diálogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) artículo de documentación.

```csharp
public class PrinterSettingsContainer
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(PrinterSettings) | Crea un contenedor paraPrinterSettings . |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | VerPaperSource deDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | VerPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | VerPaperSources . |

### Observaciones

Acceso a datos dePrinterSettings lleva mucho tiempo. `PrinterSettingsContainer` almacena en caché los parámetros dePrinterSettings , para que la impresión funcione más rápido.

### Ejemplos

Muestra cómo acceder y enumerar los orígenes y tamaños del papel de su impresora.

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

// La propiedad "PaperSizes" contiene la lista de tamaños de papel que se deben indicar a la impresora.
// Tanto PrinterSource como PrinterSize contienen una propiedad "RawKind",
// que equivale a un tipo de papel que figura en la enumeración PaperSourceKind.
// Si hay una fuente de papel con el mismo valor "RawKind" que el de la página de impresión,
// la impresora imprimirá la página utilizando la fuente y el tamaño del papel proporcionados.
// De lo contrario, la impresora utilizará de forma predeterminada la fuente designada por la propiedad "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Ver también

* espacio de nombres [Aspose.Words.Rendering](../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../)


