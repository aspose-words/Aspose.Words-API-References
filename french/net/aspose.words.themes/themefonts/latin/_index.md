---
title: ThemeFonts.Latin
linktitle: Latin
articleTitle: Latin
second_title: Aspose.Words pour .NET
description: Découvrez ThemeFonts pour les caractères latins ! Améliorez votre design grâce à des polices personnalisables qui sublimeront votre typographie et l'expérience utilisateur.
type: docs
weight: 30
url: /fr/net/aspose.words.themes/themefonts/latin/
---
## ThemeFonts.Latin property

Spécifie le nom de la police pour les caractères latins.

```csharp
public string Latin { get; set; }
```

## Exemples

Montre comment définir des couleurs et des polices personnalisées pour les thèmes.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// L'objet "Thème" nous donne accès au thème du document, une source de polices et de couleurs par défaut.
Theme theme = doc.Theme;

// Certains styles, tels que « Titre 1 » et « Sous-titre », hériteront de ces polices.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// D'autres langues peuvent également avoir leurs polices personnalisées dans ce thème.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// La propriété « Couleurs » contient la palette de couleurs de Microsoft Word,
// qui apparaît lors du changement d'ombrage ou de couleur de police.
// Appliquez des couleurs personnalisées à la palette de couleurs afin que nous puissions y accéder facilement dans Microsoft Word
// lorsque nous changeons, par exemple, la couleur de la police via "Accueil" -> "Police" -> "Couleur de la police",
// ou insérez une forme, puis définissez une couleur pour celle-ci via « Format de forme » -> « Styles de forme ».
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

// Appliquer des couleurs personnalisées aux hyperliens dans leurs états cliqués et non cliqués.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Voir également

* class [ThemeFonts](../)
* espace de noms [Aspose.Words.Themes](../../../aspose.words.themes/)
* Assemblée [Aspose.Words](../../../)
