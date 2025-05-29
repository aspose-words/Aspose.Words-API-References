---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.ThemeColors, que presenta un esquema versátil de 12 colores para mejorar el atractivo visual y la consistencia de su documento.
type: docs
weight: 7330
url: /es/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Representa el esquema de colores del tema del documento que contiene doce colores.

`ThemeColors` El objeto contiene seis colores de acento, dos colores oscuros, dos colores claros y un color para cada uno de un hipervínculo y un hipervínculo seguido.

```csharp
public class ThemeColors
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Especifica el color Acento 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Especifica el acento de color 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Especifica el acento de color 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Especifica el acento de color 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Especifica el acento de color 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Especifica el acento de color 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Especifica el color Oscuro 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Especifica el color Oscuro 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Especifica el color de un hipervínculo en el que se hizo clic. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Especifica el color de un hipervínculo. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Especifica el color Luz 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Especifica el color Claro 2. |

## Ejemplos

Muestra cómo configurar colores y fuentes personalizados para los temas.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// El objeto "Tema" nos da acceso al tema del documento, una fuente de fuentes y colores predeterminados.
Theme theme = doc.Theme;

//Algunos estilos, como "Título 1" y "Subtítulo", heredarán estas fuentes.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Otros idiomas también pueden tener sus fuentes personalizadas en este tema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// La propiedad "Colores" contiene la paleta de colores de Microsoft Word,
// que aparece al cambiar el sombreado o el color de la fuente.
// Aplicar colores personalizados a la paleta de colores para que tengamos fácil acceso a ellos en Microsoft Word
// cuando, por ejemplo, cambiamos el color de la fuente a través de "Inicio" -> "Fuente" -> "Color de fuente",
// o inserte una forma y luego establezca un color para ella a través de "Formato de forma" -> "Estilos de forma".
ThemeColors colors = theme.Colors;
colors.Dark1 = Color.MidnightBlue;
colors.Light1 = Color.PaleGreen;
colors.Dark2 = Color.Indigo;
colors.Light2 = Color.Khaki;

colors.Accent1 = Color.OrangeRed;
colors.Accent2 = Color.LightSalmon;
colors.Accent3 = Color.Yellow;
colors.Accent4 = Color.Gold;
colors.Accent5 = Color.BlueViolet;
colors.Accent6 = Color.DarkViolet;

// Aplicar colores personalizados a los hipervínculos en sus estados en los que se hizo clic y en los que no se hizo clic.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Themes](../../aspose.words.themes/)
* asamblea [Aspose.Words](../../)
