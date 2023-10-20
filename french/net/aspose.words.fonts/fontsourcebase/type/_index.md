---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: FontSourceBase Type propriété. Renvoie le type de la source de police en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Renvoie le type de la source de police.

```csharp
public abstract FontSourceType Type { get; }
```

## Exemples

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FontSourceBase](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
