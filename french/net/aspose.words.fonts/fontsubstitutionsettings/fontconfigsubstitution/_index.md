---
title: FontSubstitutionSettings.FontConfigSubstitution
linktitle: FontConfigSubstitution
articleTitle: FontConfigSubstitution
second_title: Aspose.Words pour .NET
description: Explorez FontSubstitutionSettings pour une configuration de police optimisée. Découvrez comment améliorer la typographie grâce à des règles de substitution efficaces pour un design optimal.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Paramètres liés à la règle de substitution de configuration de police.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

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

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
