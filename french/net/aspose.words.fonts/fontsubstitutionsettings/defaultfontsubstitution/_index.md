---
title: DefaultFontSubstitution
second_title: Référence de l'API Aspose.Words pour .NET
description: Paramètres liés à la règle de substitution de police par défaut.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Paramètres liés à la règle de substitution de police par défaut.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

### Exemples

Montre comment définir la règle de substitution de police par défaut.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Récupère la règle de substitution par défaut dans FontSettings.
// Cette règle remplacera toutes les polices manquantes par "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Définit le substitut de police par défaut sur "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// A l'aide d'un constructeur de document, ajoutez du texte dans une police dont nous n'avons pas besoin pour voir la substitution se produire,
// puis affichez le résultat dans un PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Voir également

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule)
* class [FontSubstitutionSettings](../../fontsubstitutionsettings)
* espace de noms [Aspose.Words.Fonts](../../fontsubstitutionsettings)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
