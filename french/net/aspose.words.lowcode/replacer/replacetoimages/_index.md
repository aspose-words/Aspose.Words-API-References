---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words pour .NET
description: Transformez sans effort vos fichiers d'entrée en remplaçant les modèles de caractères par des chaînes personnalisées et en générant des images époustouflantes avec notre méthode ReplaceToImages.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée. Restitue la sortie sous forme d'images.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

## Exemples

Montre comment remplacer une chaîne dans le document et enregistrer le résultat dans les images.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document :
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée. Restitue la sortie sous forme d'images.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

## Exemples

Montre comment remplacer une chaîne dans le document à l'aide de documents du flux et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document à l'aide de documents du flux :
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

    FindReplaceOptions options = new FindReplaceOptions();
    options.FindWholeWordsOnly = false;
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Remplace toutes les occurrences d'un modèle d'expression régulière spécifié par une chaîne de remplacement dans le fichier d'entrée. Restitue la sortie sous forme d'images.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document et enregistrer le résultat dans les images.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document :
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Remplace toutes les occurrences d'un modèle d'expression régulière spécifié par une chaîne de remplacement dans le fichier d'entrée. Restitue la sortie sous forme d'images.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux et enregistrer le résultat dans des images.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux :
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
