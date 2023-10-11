---
title: FontSourceBase.WarningCallback
second_title: Referencia de API de Aspose.Words para .NET
description: FontSourceBase propiedad. Se llama durante el procesamiento del origen de la fuente cuando se detecta un problema que podría provocar una pérdida de fidelidad del formato.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Se llama durante el procesamiento del origen de la fuente cuando se detecta un problema que podría provocar una pérdida de fidelidad del formato.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Ejemplos

Muestra cómo llamar a una devolución de llamada de advertencia cuando se trabaja con las fuentes de fuentes.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Obtenga la lista de fuentes para llamar a la devolución de llamada de advertencia.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Se llama cada vez que ocurre una advertencia durante el procesamiento de la fuente de fuente.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Ver también

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontsourcebase/)
* asamblea [Aspose.Words](../../../)


