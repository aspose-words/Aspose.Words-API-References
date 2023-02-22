---
title: FontSourceBase.Priority
second_title: Référence de l'API Aspose.Words pour .NET
description: FontSourceBase propriété. Renvoie la priorité de la source de la police.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Renvoie la priorité de la source de la police.

```csharp
public int Priority { get; }
```

### Remarques

Cette valeur est utilisée lorsqu'il existe des polices avec le même nom de famille et le même style dans différentes sources de polices. Dans ce cas, Aspose.Words sélectionne la police de la source avec la valeur de priorité la plus élevée.

La valeur par défaut est 0.

### Exemples

Montre comment utiliser un fichier de police dans le système de fichiers local comme source de police.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Voir également

* class [FontSourceBase](../)
* espace de noms [Aspose.Words.Fonts](../../fontsourcebase/)
* Assemblée [Aspose.Words](../../../)


