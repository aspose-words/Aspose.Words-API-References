---
title: TableSubstitutionRule.LoadLinuxSettings
linktitle: LoadLinuxSettings
articleTitle: LoadLinuxSettings
second_title: Aspose.Words pour .NET
description: Chargez facilement des paramètres de substitution de table prédéfinis pour Linux avec la méthode LoadLinuxSettings. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule.LoadLinuxSettings method

Charge les paramètres de substitution de table prédéfinis pour la plate-forme Linux.

```csharp
public void LoadLinuxSettings()
```

## Exemples

Montre comment accéder aux tables de substitution de polices pour Windows et Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Créez une nouvelle règle de substitution de table et chargez la table de substitution de polices Microsoft Windows par défaut.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// Sous Windows, le substitut par défaut de la police « Times New Roman CE » est « Times New Roman ».
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Nous pouvons enregistrer le tableau sous la forme d'un document XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux a sa propre table de substitution.
// Il existe plusieurs polices de substitution pour « Times New Roman CE ».
// Si le premier substitut, « FreeSerif », n'est pas non plus disponible,
// cette règle parcourra les autres dans le tableau jusqu'à ce qu'elle en trouve une disponible.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Enregistrez la table de substitution Linux sous la forme d'un document XML à l'aide d'un flux.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Voir également

* class [TableSubstitutionRule](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
