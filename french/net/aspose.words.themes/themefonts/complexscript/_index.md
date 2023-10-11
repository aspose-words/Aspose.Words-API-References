---
title: ThemeFonts.ComplexScript
second_title: Référence de l'API Aspose.Words pour .NET
description: ThemeFonts propriété. Spécifie le nom de la police pour les caractères ComplexScript.
type: docs
weight: 10
url: /fr/net/aspose.words.themes/themefonts/complexscript/
---
## ThemeFonts.ComplexScript property

Spécifie le nom de la police pour les caractères ComplexScript.

```csharp
public string ComplexScript { get; set; }
```

### Exemples

Montre comment définir des couleurs et des polices personnalisées pour les thèmes.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// L'objet "Theme" nous donne accès au thème du document, source de polices et de couleurs par défaut.
Theme theme = doc.Theme;

// Certains styles, tels que "Titre 1" et "Sous-titre", hériteront de ces polices.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// D'autres langues peuvent également avoir leurs polices personnalisées dans ce thème.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// La propriété "Couleurs" contient la palette de couleurs de Microsoft Word,
// qui apparaît lors du changement d'ombrage ou de couleur de police.
// Applique des couleurs personnalisées à la palette de couleurs afin d'y accéder facilement dans Microsoft Word
// quand on change par exemple la couleur de la police via "Accueil" -> "Police" -> "Couleur de la police",
// ou insérez une forme, puis définissez-lui une couleur via "Format de forme" -> "Styles de forme".
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

// Applique des couleurs personnalisées aux hyperliens dans leurs états cliqués et non cliqués.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Voir également

* class [ThemeFonts](../)
* espace de noms [Aspose.Words.Themes](../../themefonts/)
* Assemblée [Aspose.Words](../../../)


