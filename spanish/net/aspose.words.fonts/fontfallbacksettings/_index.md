---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Fonts.FontFallbackSettings para obtener opciones de reserva de fuentes personalizables, lo que garantiza una representación perfecta del documento y una visualización de texto mejorada.
type: docs
weight: 3330
url: /es/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Especifica la configuración del mecanismo de reserva de fuentes.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class FontFallbackSettings
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Crea automáticamente la configuración de respaldo escaneando las fuentes disponibles. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | Carga la configuración de respaldo desde la secuencia XML. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | Carga la configuración de reserva de fuentes desde el archivo XML. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Carga configuraciones de respaldo predefinidas que imitan el respaldo de Microsoft Word y utilizan fuentes de Microsoft Office. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Carga configuraciones de respaldo predefinidas que utilizan fuentes de Google Noto. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Guarda la configuración de respaldo actual en la transmisión. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Guarda la configuración de respaldo actual en un archivo. |

## Observaciones

De manera predeterminada, las configuraciones de respaldo se inicializan con configuraciones predefinidas que imitan la configuración de respaldo de Microsoft Word.

## Ejemplos

Muestra cómo distribuir fuentes de respaldo en rangos de códigos de caracteres Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Configure nuestros ajustes de fuentes para obtener fuentes solo de la carpeta "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Llamar al método "BuildAutomatic" generará un esquema de respaldo que
// distribuye fuentes accesibles en tantos códigos de caracteres Unicode como sea posible.
// En nuestro caso, solo tiene acceso a un puñado de fuentes dentro de la carpeta "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// También podemos cargar un esquema de sustitución personalizado desde un archivo como este.
// Este esquema aplica la fuente "AllegroOpen" en los bloques Unicode "0000-00ff", la fuente "AllegroOpen" en los bloques "0100-024f",
// y la fuente "M+ 2m" en todos los demás rangos que otras fuentes del esquema no cubren.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Cree un generador de documentos y configure su fuente en una que no exista en ninguna de nuestras fuentes.
// Nuestra configuración de fuente invocará el esquema de respaldo para los caracteres que escribamos usando la fuente no disponible.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Utilice el generador para imprimir todos los caracteres Unicode desde 0x0021 hasta 0x052F,
// con líneas descriptivas que dividen los bloques Unicode que definimos en nuestro esquema de reserva de fuentes personalizado.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
