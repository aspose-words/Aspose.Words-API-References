---
title: FontFallbackSettings.Load
second_title: Referencia de API de Aspose.Words para .NET
description: FontFallbackSettings método. Carga la configuración de reserva de fuentes desde el archivo XML.
type: docs
weight: 20
url: /es/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(string) {#load_1}

Carga la configuración de reserva de fuentes desde el archivo XML.

```csharp
public void Load(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo de entrada. |

### Ejemplos

Muestra cómo cargar y guardar configuraciones de reserva de fuentes hacia/desde un documento XML en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Carga un documento XML que define un conjunto de configuraciones de reserva de fuentes.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Guarde la configuración de reserva de fuente actual de nuestro documento como un documento XML.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Ver también

* class [FontFallbackSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontfallbacksettings/)
* asamblea [Aspose.Words](../../../)

---

## Load(Stream) {#load}

Carga la configuración alternativa desde la secuencia XML.

```csharp
public void Load(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Flujo de entrada. |

### Ejemplos

Muestra cómo cargar y guardar configuraciones de reserva de fuentes hacia/desde una secuencia.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Carga un documento XML que define un conjunto de configuraciones de reserva de fuentes.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utilice una secuencia para guardar la configuración de reserva de fuente actual de nuestro documento como un documento XML.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Ver también

* class [FontFallbackSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontfallbacksettings/)
* asamblea [Aspose.Words](../../../)


