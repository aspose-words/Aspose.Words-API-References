---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words pour .NET
description: Comparez facilement deux documents grâce à notre méthode de comparaison. Enregistrez les différences et suivez les modifications et les mises à jour de format dans un seul fichier de sortie.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant des modifications sous forme de plusieurs révisions d'édition et de format.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | String | Le document original. |
| v2 | String | Le document modifié. |
| outputFileName | String | Le nom du fichier de sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment comparer simplement des documents.

```csharp
// Il existe plusieurs façons de comparer des documents :
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Voir également

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié dans le format d'enregistrement fourni, produisant des modifications sous forme de plusieurs révisions d'édition et de format.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | String | Le document original. |
| v2 | String | Le document modifié. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment comparer simplement des documents.

```csharp
// Il existe plusieurs façons de comparer des documents :
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié dans le format d'enregistrement fourni, produisant des modifications sous forme de plusieurs révisions d'édition et de format.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | String | Le document original. |
| v2 | String | Le document modifié. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni dans le format d'enregistrement spécifié, produisant des modifications sous forme de nombre de révisions d'édition et de format.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | Stream | Le document original. |
| v2 | Stream | Le document modifié. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment comparer les documents du flux.

```csharp
// Il existe plusieurs façons de comparer les documents du flux :
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni dans le format d'enregistrement spécifié, produisant des modifications sous forme de nombre de révisions d'édition et de format.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | Stream | Le document original. |
| v2 | Stream | Le document modifié. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
