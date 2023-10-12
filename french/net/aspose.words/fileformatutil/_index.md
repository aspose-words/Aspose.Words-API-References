---
title: Class FileFormatUtil
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.FileFormatUtil classe. Fournit des méthodes utilitaires pour travailler avec des formats de fichiers telles que la détection du format de fichier ou la conversion dextensions de fichier vers/depuis des énumérations de format de fichier.
type: docs
weight: 2820
url: /fr/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Fournit des méthodes utilitaires pour travailler avec des formats de fichiers, telles que la détection du format de fichier ou la conversion d'extensions de fichier vers/depuis des énumérations de format de fichier.

Pour en savoir plus, visitez le[Détecter le format de fichier et vérifier la compatibilité des formats](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) article documentaire.

```csharp
public static class FileFormatUtil
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(string) | Convertit le type de contenu IANA en une valeur énumérée au format de chargement. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(string) | Convertit le type de contenu IANA en une valeur énumérée au format de sauvegarde. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(Stream) | Détecte et renvoie les informations sur le format d'un document stocké dans un flux. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(string) | Détecte et renvoie les informations sur le format d'un document stocké dans un fichier disque. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(string) | Convertit une extension de nom de fichier en un[`SaveFormat`](../saveformat/) valeur. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(ImageType) | Convertit une valeur énumérée de type d'image Aspose.Words en une extension de fichier. L'extension renvoyée est une chaîne minuscule précédée d'un point. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(LoadFormat) | Convertit une valeur énumérée au format de chargement en une extension de fichier. L'extension renvoyée est une chaîne minuscule précédée d'un point. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(LoadFormat) | Convertit un[`LoadFormat`](../loadformat/) valeur à un[`SaveFormat`](../saveformat/) valeur si possible. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(SaveFormat) | Convertit une valeur énumérée au format de sauvegarde en une extension de fichier. L'extension renvoyée est une chaîne minuscule précédée d'un point. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(SaveFormat) | Convertit un[`SaveFormat`](../saveformat/) valeur à un[`LoadFormat`](../loadformat/) valeur si possible. |

### Exemples

Montre comment détecter l'encodage dans un fichier HTML.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La propriété Encoding est utilisée uniquement lorsque nous créons un objet FileFormatInfo pour un document HTML.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


