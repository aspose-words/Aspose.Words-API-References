---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.FontConfigSubstitutionRule pour une gestion et une personnalisation fluides des polices dans vos documents. Améliorez le style de votre texte dès aujourd'hui !
type: docs
weight: 3300
url: /fr/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Règle de substitution de configuration de police.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## Propriétés

| Nom | La description |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | Spécifie si la règle est activée ou non. |

## Méthodes

| Nom | La description |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | Vérifiez si l'utilitaire fontconfig est disponible ou non. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | Réinitialise le cache des résultats d'appel de fontconfig. |

## Remarques

Cette règle utilise l'utilitaire fontconfig sur Linux (et autres plates-formes de type Unix) pour obtenir la substitution si la police d'origine n'est pas disponible.

Si l'utilitaire fontconfig n'est pas disponible, cette règle sera ignorée.

## Exemples

Affiche la substitution de configuration de police dépendante du système d'exploitation.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// L'objet FontConfigSubstitutionRule fonctionne différemment sur les plates-formes Windows/non Windows.
// Sous Windows, il n'est pas disponible.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Sous Linux/Mac, nous y aurons accès, et pourrons effectuer des opérations.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Voir également

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
