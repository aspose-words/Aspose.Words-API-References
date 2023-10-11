---
title: FolderFontSource.FolderFontSource
second_title: Référence de l'API Aspose.Words pour .NET
description: FolderFontSource constructeur. Directeur.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(string, bool) {#constructor}

Directeur.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| folderPath | String | Chemin d'accès au dossier. |
| scanSubfolders | Boolean | Détermine s’il faut ou non analyser les sous-dossiers. |

### Exemples

Montre comment utiliser un dossier système local contenant des polices comme source de polices.

```csharp
// Crée une source de police à partir d'un dossier contenant des fichiers de police.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Voir également

* class [FolderFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../folderfontsource/)
* Assemblée [Aspose.Words](../../../)

---

## FolderFontSource(string, bool, int) {#constructor_1}

Directeur.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| folderPath | String | Chemin d'accès au dossier. |
| scanSubfolders | Boolean | Détermine s’il faut ou non analyser les sous-dossiers. |
| priority | Int32 | Priorité de la source de police. Voir le[`Priority`](../../fontsourcebase/priority/) Description de la propriété pour plus d'informations. |

### Exemples

Montre comment utiliser un dossier système local contenant des polices comme source de polices.

```csharp
// Crée une source de police à partir d'un dossier contenant des fichiers de police.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Voir également

* class [FolderFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../folderfontsource/)
* Assemblée [Aspose.Words](../../../)


