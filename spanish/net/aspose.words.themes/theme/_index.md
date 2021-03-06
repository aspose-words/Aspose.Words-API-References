---
title: Theme
second_title: Referencia de API de Aspose.Words para .NET
description: Representa el tema del documento y brinda acceso a las partes principales del tema incluidasMajorFonts./theme/majorfonts MinorFonts./theme/minorfonts yColors./theme/colors
type: docs
weight: 6160
url: /es/net/aspose.words.themes/theme/
---
## Theme class

Representa el tema del documento y brinda acceso a las partes principales del tema, incluidas[`MajorFonts`](./majorfonts) ,[`MinorFonts`](./minorfonts) y[`Colors`](./colors)

```csharp
public class Theme
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Theme](theme)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Colors](../../aspose.words.themes/theme/colors) { get; } | Permite especificar el conjunto de colores del tema para el documento. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts) { get; } | Permite especificar el conjunto de fuentes principales para diferentes idiomas. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts) { get; } | Permite especificar el conjunto de fuentes menores para diferentes idiomas. |

### Ejemplos

Muestra cómo establecer colores y fuentes personalizados para los temas.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// El objeto "Tema" nos da acceso al tema del documento, una fuente de fuentes y colores predeterminados.
Theme theme = doc.Theme;

// Algunos estilos, como "Título 1" y "Subtítulo", heredarán estas fuentes.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Otros idiomas también pueden tener sus fuentes personalizadas en este tema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// La propiedad "Colores" contiene la paleta de colores de Microsoft Word,
// que aparece al cambiar el sombreado o el color de la fuente.
// Aplique colores personalizados a la paleta de colores para que tengamos fácil acceso a ellos en Microsoft Word
// cuando, por ejemplo, cambiamos el color de la fuente a través de "Inicio" -> "Fuente" -> "Color de fuente",
// o inserte una forma, y luego establezca un color para ella a través de "Formato de forma" -> "Estilos de forma".
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

// Aplique colores personalizados a los hipervínculos en sus estados de clic y no clic.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Themes](../../aspose.words.themes)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
