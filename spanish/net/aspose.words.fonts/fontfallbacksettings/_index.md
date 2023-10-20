---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words para .NET
description: Aspose.Words.Fonts.FontFallbackSettings clase. Especifica la configuración del mecanismo de reserva de fuentes en C#.
type: docs
weight: 2900
url: /es/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Especifica la configuración del mecanismo de reserva de fuentes.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) artículo de documentación.

```csharp
public class FontFallbackSettings
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Crea automáticamente la configuración alternativa escaneando las fuentes disponibles. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | Carga la configuración alternativa desde la secuencia XML. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | Carga la configuración de reserva de fuentes desde el archivo XML. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Carga configuraciones de respaldo predefinidas que imitan el respaldo de Microsoft Word y utilizan fuentes de Microsoft Office. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Carga configuraciones de respaldo predefinidas que utilizan fuentes Google Noto. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Guarda la configuración alternativa actual en la transmisión. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Guarda la configuración alternativa actual en un archivo. |

## Observaciones

De forma predeterminada, la configuración de respaldo se inicializa con configuraciones predefinidas que imitan el respaldo de Microsoft Word.

## Ejemplos

Muestra cómo distribuir fuentes alternativas en rangos de códigos de caracteres Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Configure nuestra configuración de fuentes para obtener fuentes solo desde la carpeta "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Llamar al método "BuildAutomatic" generará un esquema alternativo que
// distribuye fuentes accesibles en tantos códigos de caracteres Unicode como sea posible.
// En nuestro caso, solo tiene acceso a un puñado de fuentes dentro de la carpeta "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// También podemos cargar un esquema de sustitución personalizado desde un archivo como este.
// Este esquema aplica la fuente "AllegroOpen" en los bloques Unicode "0000-00ff", la fuente "AllegroOpen" en "0100-024f",
// y la fuente "M+ 2m" en todos los demás rangos que otras fuentes del esquema no cubren.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Cree un generador de documentos y establezca su fuente en una que no exista en ninguna de nuestras fuentes.
// Nuestra configuración de fuente invocará el esquema alternativo para los caracteres que escribimos usando la fuente no disponible.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Usa el constructor para imprimir cada carácter Unicode desde 0x0021 hasta 0x052F,
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
