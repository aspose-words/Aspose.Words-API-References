---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words pour .NET
description: Divisez facilement vos documents en plusieurs sections grâce à notre méthode flexible de fractionnement. Enregistrez-les au format de votre choix pour une gestion simplifiée des fichiers !
type: docs
weight: 40
url: /fr/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Divise un document en plusieurs parties selon les options de division spécifiées et enregistre les parties obtenues dans des fichiers. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie utilisé pour générer le nom de fichier pour les parties du document à l'aide de la règle « outputFile_partIndex.extension » |
| options | SplitOptions | Options de fractionnement de document. |

## Exemples

Montre comment diviser un document par pages.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Voir également

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie utilisé pour générer le nom de fichier pour les parties du document à l'aide de la règle « outputFile_partIndex.extension » |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| options | SplitOptions | Options de fractionnement de document. |

## Exemples

Montre comment diviser un document par pages.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie utilisé pour générer le nom de fichier pour les parties du document à l'aide de la règle « outputFile_partIndex.extension » |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| options | SplitOptions | Options de fractionnement de document. |

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Divise un document d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme de tableau de flux dans le format d'enregistrement spécifié.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| options | SplitOptions | Options de fractionnement de document. |

## Exemples

Montre comment diviser le document du flux par pages.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Divise un document d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme de tableau de flux dans le format d'enregistrement spécifié.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| options | SplitOptions | Options de fractionnement de document. |

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
