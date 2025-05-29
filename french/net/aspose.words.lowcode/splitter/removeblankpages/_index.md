---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words pour .NET
description: Supprimez facilement les pages vides de vos documents grâce à la méthode Splitter RemoveBlankPages. Gagnez du temps et optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Supprime les pages vides du document et enregistre le résultat. Renvoie la liste des numéros de page supprimés.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |

### Return_Value

La liste des numéros de page a été considérée comme vide et supprimée.

## Exemples

Montre comment supprimer les pages vides du document.

```csharp
// Il existe plusieurs façons de supprimer les pages vides du document :
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Voir également

* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Supprime les pages vides du document et enregistre le résultat au format spécifié. Renvoie la liste des numéros de page supprimés.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |

### Return_Value

La liste des numéros de page a été considérée comme vide et supprimée.

## Exemples

Montre comment supprimer les pages vides du document.

```csharp
// Il existe plusieurs façons de supprimer les pages vides du document :
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Supprime les pages vides du document et enregistre le résultat au format spécifié. Renvoie la liste des numéros de page supprimés.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

### Return_Value

La liste des numéros de page a été considérée comme vide et supprimée.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Supprime les pages vierges d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format spécifié. Renvoie la liste des numéros de page supprimés.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |

### Return_Value

La liste des numéros de page a été considérée comme vide et supprimée.

## Exemples

Montre comment supprimer les pages vides du document à partir du flux.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Supprime les pages vierges d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format spécifié. Renvoie la liste des numéros de page supprimés.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

### Return_Value

La liste des numéros de page a été considérée comme vide et supprimée.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
