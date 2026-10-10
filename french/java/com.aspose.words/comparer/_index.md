---
title: "Comparer"
linktitle: "Comparer"
second_title: "Aspose.Words pour Java"
description: "Fournit des méthodes destinées à comparer des documents en Java."
type: docs
weight: 114
url: /fr/java/com.aspose.words/comparer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Comparer extends Processor
```

Fournit des méthodes destinées à comparer des documents.
## Méthodes

| Méthode | Description |
| --- | --- |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant les changements sous forme d'un nombre de révisions d'édition et de format. |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant les changements sous forme d'un nombre de révisions d'édition et de format. |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date) |  |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant les changements sous forme d'un nombre de révisions d'édition et de format. |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant les changements sous forme d'un nombre de révisions d'édition et de format. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | Compare deux documents et enregistre les différences sous forme d'images. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Compare deux documents et enregistre les différences sous forme d'images. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | Compare deux documents et enregistre les différences sous forme d'images. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Compare deux documents et enregistre les différences sous forme d'images. |
| [create()](#create) | Crée une nouvelle instance du processeur de conversion. |
| [create(ComparerContext context)](#create-com.aspose.words.ComparerContext) | Crée une nouvelle instance du processeur de comparaison. |
| [execute()](#execute) | Exécute l'action du processeur. |
| [from(InputStream input)](#from-java.io.InputStream) | Spécifie le document d'entrée pour le traitement. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [from(String input)](#from-java.lang.String) | Spécifie le document d'entrée pour le traitement. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| auteur | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| auteur | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| auteur | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| auteur | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)
```


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant les changements sous forme d'un nombre de révisions d'édition et de format.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String | Le document original. |
| v2 | java.lang.String | Le document modifié. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement de la sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant les changements sous forme d'un nombre de révisions d'édition et de format.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String | Le document original. |
| v2 | java.lang.String | Le document modifié. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement de la sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Options de comparaison de documents. |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| auteur | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| auteur | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime)
```


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant les changements sous forme d'un nombre de révisions d'édition et de format.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String | Le document original. |
| v2 | java.lang.String | Le document modifié. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)
```


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant les changements sous forme d'un nombre de révisions d'édition et de format.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

 **Examples:** 

Montre comment comparer simplement des documents.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.1.docx", "Author", new Date());
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.2.docx", SaveFormat.DOCX, "Author", new Date());
 CompareOptions options = new CompareOptions();
 options.setIgnoreCaseChanges(true);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.3.docx", "Author", new Date(), options);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.4.docx", SaveFormat.DOCX, "Author", new Date(), options);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String | Le document original. |
| v2 | java.lang.String | Le document modifié. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Options de comparaison de documents. |

### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique du résultat rendue comme une image.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.io.InputStream | Le document original. |
| v2 | java.io.InputStream | Le document modifié. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Options d'enregistrement d'image de la sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |

**Returns:**
java.io.OutputStream[]
### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique du résultat rendue comme une image.

 **Examples:** 

Montre comment comparer des documents et enregistrer les résultats sous forme d'images.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 OutputStream[] pages = Comparer.compareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date());

 try (FileInputStream firstStreamIn = new FileInputStream(firstDoc)) {
     try (FileInputStream secondStreamIn = new FileInputStream(secondDoc)) {
         CompareOptions compareOptions = new CompareOptions();
         compareOptions.setIgnoreCaseChanges(true);
         pages = Comparer.compareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date(), compareOptions);
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.io.InputStream | Le document original. |
| v2 | java.io.InputStream | Le document modifié. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Options d'enregistrement d'image de la sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Options de comparaison de documents. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique du résultat rendue comme une image.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String | Le document original. |
| v2 | java.lang.String | Le document modifié. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Options d'enregistrement d'image de la sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique du résultat rendue comme une image.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | java.lang.String | Le document original. |
| v2 | java.lang.String | Le document modifié. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Options d'enregistrement d'image de la sortie. |
| auteur | java.lang.String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | java.util.Date | La date et l'heure à utiliser pour les révisions. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Options de comparaison de documents. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static Comparer create()
```


Crée une nouvelle instance du processeur de conversion.

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### create(ComparerContext context) {#create-com.aspose.words.ComparerContext}
```
public static Comparer create(ComparerContext context)
```


Crée une nouvelle instance du processeur de comparaison.

 **Examples:** 

Montre comment comparer simplement des documents en utilisant le contexte.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Montre comment comparer des documents depuis le flux en utilisant le contexte.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| context | [ComparerContext](../../com.aspose.words/comparercontext/) |  |

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### execute() {#execute}
```
public void execute()
```


Exécute l'action du processeur.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

Montre comment convertir des documents du flux avec une seule ligne de code en utilisant le contexte.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.io.InputStream | Flux du document d'entrée. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

 **Examples:** 

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

Montre comment convertir des documents du flux avec une seule ligne de code en utilisant le contexte.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.io.InputStream | Flux du document d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options de chargement facultatives utilisées pour charger le document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.lang.String | Nom de fichier du document d'entrée. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.lang.String | Nom de fichier du document d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options de chargement facultatives utilisées pour charger le document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Spécifie le fichier de sortie pour le processeur.

 **Remarks:** 

Si la sortie se compose de plusieurs fichiers, le nom de fichier de sortie spécifié est utilisé pour générer le nom de fichier de chaque partie selon la règle : 'outputFile\_partIndex.extension'.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String | Nom du fichier de sortie. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Spécifie le fichier de sortie pour le processeur.

 **Remarks:** 

Si la sortie se compose de plusieurs fichiers, le nom de fichier de sortie spécifié est utilisé pour générer le nom de fichier de chaque partie selon la règle : 'outputFile\_partIndex.extension'.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String | Nom du fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Options d'enregistrement facultatives. Si non spécifiées, le format d'enregistrement est déterminé par l'extension du fichier. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
