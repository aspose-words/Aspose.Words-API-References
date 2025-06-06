---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words para .NET
description: Descubra el método FontFallbackSettings LoadMsOfficeFallbackSettings para implementar fácilmente configuraciones de respaldo similares a las de Microsoft Word con fuentes de Office para una integración perfecta.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Carga configuraciones de respaldo predefinidas que imitan el respaldo de Microsoft Word y utilizan fuentes de Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Ejemplos

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
