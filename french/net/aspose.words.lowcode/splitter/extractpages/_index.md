---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words pour .NET
description: Extrayez facilement des pages spécifiques de n'importe quel document grâce à notre méthode Splitter ExtractPages. Enregistrez-les au format souhaité pour un accès facile !
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Extrait une plage de pages spécifiée d'un fichier document et enregistre les pages extraites dans un nouveau fichier. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| startPageIndex | Int32 | L'index de base zéro de la première page à extraire. |
| pageCount | Int32 | Nombre de pages à extraire. |

## Exemples

Montre comment extraire des pages du document.

```csharp
// Il existe plusieurs façons d'extraire des pages du document :
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Voir également

* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| startPageIndex | Int32 | L'index de base zéro de la première page à extraire. |
| pageCount | Int32 | Nombre de pages à extraire. |

## Exemples

Montre comment extraire des pages du document.

```csharp
// Il existe plusieurs façons d'extraire des pages du document :
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| startPageIndex | Int32 | L'index de base zéro de la première page à extraire. |
| pageCount | Int32 | Nombre de pages à extraire. |

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Extrait une plage spécifiée de pages d'un flux de documents et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| startPageIndex | Int32 | L'index de base zéro de la première page à extraire. |
| pageCount | Int32 | Nombre de pages à extraire. |

## Exemples

Montre comment extraire des pages du document à partir du flux.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Extrait une plage spécifiée de pages d'un flux de documents et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| startPageIndex | Int32 | L'index de base zéro de la première page à extraire. |
| pageCount | Int32 | Nombre de pages à extraire. |

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
