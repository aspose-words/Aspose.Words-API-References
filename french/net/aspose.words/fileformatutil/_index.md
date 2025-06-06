---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words pour .NET
description: Gérez facilement les formats de fichiers avec Aspose.Words.FileFormatUtil. Détectez les formats et convertissez les extensions en toute simplicité pour une productivité accrue.
type: docs
weight: 3230
url: /fr/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Fournit des méthodes utilitaires pour travailler avec des formats de fichiers, tels que la détection du format de fichier ou la conversion des extensions de fichiers vers/depuis les énumérations de formats de fichiers.

Pour en savoir plus, visitez le[Détecter le format de fichier et vérifier la compatibilité des formats](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) article de documentation.

```csharp
public static class FileFormatUtil
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Convertit le type de contenu IANA en une valeur énumérée au format de chargement. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Convertit le type de contenu IANA en une valeur énumérée au format de sauvegarde. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Détecte et renvoie les informations sur un format d'un document stocké dans un flux. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Détecte et renvoie les informations sur le format d'un document stocké dans un fichier disque. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Convertit une extension de nom de fichier en un[`SaveFormat`](../saveformat/) valeur. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Convertit une valeur énumérée de type image Aspose.Words en extension de fichier. L'extension renvoyée est une chaîne en minuscules précédée d'un point. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Convertit une valeur énumérée au format de chargement en extension de fichier. L'extension renvoyée est une chaîne en minuscules précédée d'un point. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Convertit un[`LoadFormat`](../loadformat/) valeur à un[`SaveFormat`](../saveformat/) valeur si possible. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Convertit une valeur énumérée d'un format d'enregistrement en extension de fichier. L'extension renvoyée est une chaîne en minuscules précédée d'un point. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Convertit un[`SaveFormat`](../saveformat/) valeur à un[`LoadFormat`](../loadformat/) valeur si possible. |

## Exemples

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
