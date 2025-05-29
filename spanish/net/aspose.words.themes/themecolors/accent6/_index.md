---
title: ThemeColors.Accent6
linktitle: Accent6
articleTitle: Accent6
second_title: Aspose.Words para .NET
description: Descubre ThemeColors Accent6. Crea fácilmente tu diseño con opciones de colores vibrantes para un impacto visual impactante. ¡Mejora tus proyectos sin esfuerzo!
type: docs
weight: 60
url: /es/net/aspose.words.themes/themecolors/accent6/
---
## ThemeColors.Accent6 property

Especifica el acento de color 6.

```csharp
public Color Accent6 { get; set; }
```

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

* class [ThemeColors](../)
* espacio de nombres [Aspose.Words.Themes](../../../aspose.words.themes/)
* asamblea [Aspose.Words](../../../)
