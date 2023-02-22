---
title: Enum ThemeColor
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Themes.ThemeColor enumeración. Especifica los colores del tema para los temas del documento.
type: docs
weight: 6170
url: /es/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

Especifica los colores del tema para los temas del documento.

```csharp
public enum ThemeColor
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | Sin color. |
| Dark1 | `0` | Color principal oscuro 1. |
| Light1 | `1` | Color principal luz 1. |
| Dark2 | `2` | Color principal oscuro 2. |
| Light2 | `3` | Color principal luz 2. |
| Accent1 | `4` | Color de acento 1. |
| Accent2 | `5` | Color de acento 2. |
| Accent3 | `6` | Color de acento 3. |
| Accent4 | `7` | Color de acento 4. |
| Accent5 | `8` | Color de acento 5. |
| Accent6 | `9` | Color de acento 6. |
| Hyperlink | `10` | Hipervínculo color. |
| FollowedHyperlink | `11` | Color de hipervínculo seguido. |
| Text1 | `12` | Color de texto 1. |
| Text2 | `13` | Color de texto 2. |
| Background1 | `14` | Color de fondo 1. |
| Background2 | `15` | Color de fondo 2. |

### Observaciones

El color de tema especificado es una referencia a uno de los colores de tema predefinidos, ubicado en la parte Tema del documento , que permite que la información de color se establezca centralmente en el documento.

### Ejemplos

Muestra cómo crear y utilizar un estilo temático.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Crea un estilo con las propiedades de la fuente del tema.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Muestra cómo trabajar con fuentes y colores temáticos.

```csharp
Document doc = new Document();

// Definir fuentes para usos de idiomas por defecto.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Podemos usar la fuente y el color del tema en lugar de los valores predeterminados.
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.AreEqual(ThemeFont.Minor, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.Accent2, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// Hay varias formas de restablecer la fuente y el color.
// 1 - Configurando ThemeFont.None/ThemeColor.None:
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 2 - Al establecer nombres de fuentes/colores que no sean del tema:
font.Name = "Arial";
font.Color = Color.Blue;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Arial", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Arial", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Arial", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Arial", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Arial", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Blue.ToArgb(), font.Color.ToArgb());
```

### Ver también

* espacio de nombres [Aspose.Words.Themes](../../aspose.words.themes/)
* asamblea [Aspose.Words](../../)


