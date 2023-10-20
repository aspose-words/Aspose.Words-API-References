---
title: PrinterSettingsContainer.DefaultPageSettingsPaperSource
linktitle: DefaultPageSettingsPaperSource
articleTitle: DefaultPageSettingsPaperSource
second_title: Aspose.Words para .NET
description: PrinterSettingsContainer DefaultPageSettingsPaperSource propiedad. VerPaperSource deDefaultPageSettings  en C#.
type: docs
weight: 20
url: /es/net/aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/
---
## PrinterSettingsContainer.DefaultPageSettingsPaperSource property

VerPaperSource deDefaultPageSettings .

```csharp
public PaperSource DefaultPageSettingsPaperSource { get; }
```

## Ejemplos

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

* class [PrinterSettingsContainer](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
