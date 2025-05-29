---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words para .NET
description: Descubra cómo mejorar su tipografía con el método LoadNotoFallbackSettings de FontFallbackSettings, utilizando fuentes de Google Noto para una visualización de texto perfecta.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Carga configuraciones de respaldo predefinidas que utilizan fuentes de Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

## Ejemplos

Muestra cómo agregar configuraciones de reserva de fuentes predefinidas para las fuentes de Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// Estas son fuentes gratuitas licenciadas bajo la Licencia de fuente abierta SIL.
//Podemos descargar las fuentes aquí:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Tenga en cuenta que las configuraciones predefinidas solo utilizan fuentes Noto de estilo Sans con peso regular.
//Algunas de las fuentes Noto utilizan funciones tipográficas avanzadas.
// Es posible que las fuentes con tipografía avanzada no se representen correctamente, ya que Aspose.Words actualmente no las admite.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Muestra cómo cargar configuraciones de fuentes de reserva predefinidas.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Guarde el esquema de fuente predeterminado en un documento XML.
// Por ejemplo, uno de los elementos tiene un valor de "0C00-0C7F" para Range y un valor "Vani" correspondiente para FallbackFonts.
// Esto significa que si la fuente que utiliza algún texto no tiene símbolos para el bloque Unicode 0x0C00-0x0C7F,
// el esquema de respaldo utilizará símbolos del sustituto de fuente "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// A continuación se muestran dos esquemas de reserva de fuentes predefinidos entre los que podemos elegir.
// 1 - Utilice el esquema predeterminado de Microsoft Office, que es el mismo que el predeterminado:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Utilice el esquema creado a partir de las fuentes de Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Ver también

* class [FontFallbackSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
