---
title: Type
second_title: Référence de l'API Aspose.Words pour .NET
description: Renvoie le type de la source de la police.
type: docs
weight: 40
url: /fr/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

Renvoie le type de la source de la police.

```csharp
public override FontSourceType Type { get; }
```

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

* enum [FontSourceType](../../fontsourcetype)
* class [FileFontSource](../../filefontsource)
* espace de noms [Aspose.Words.Fonts](../../filefontsource)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->