---
title: Replacer.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words pour .NET
description: Remplacez facilement toutes les occurrences d'une chaîne spécifique dans votre fichier d'entrée grâce à la méthode Replacer. Simplifiez votre édition de texte dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/replacer/replace/
---
## Replace(*string, string, string, string*) {#replace_8}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée.

```csharp
public static int Replace(string inputFileName, string outputFileName, string pattern, 
    string replacement)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplacer une chaîne dans le document.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document :
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Voir également

* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_4}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplacer une chaîne dans le document.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document :
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_6}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée, avec le format de sauvegarde spécifié et des options supplémentaires.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment remplacer une chaîne dans le document à l'aide de documents du flux.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document à l'aide de documents du flux :
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        FindReplaceOptions options = new FindReplaceOptions();
        options.FindWholeWordsOnly = false;
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, options);
    }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_2}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée, avec le format de sauvegarde spécifié et des options supplémentaires.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*string, string, Regex, string*) {#replace_9}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée à l'aide d'une expression régulière.

```csharp
public static int Replace(string inputFileName, string outputFileName, Regex pattern, 
    string replacement)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document :
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Voir également

* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_5}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée à l'aide d'une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document :
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_7}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée à l'aide d'une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée à l'aide d'une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux :
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée à l'aide d'une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
