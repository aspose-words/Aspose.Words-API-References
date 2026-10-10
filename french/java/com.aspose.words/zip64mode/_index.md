---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words pour Java"
description: "Spécifie quand utiliser les extensions de format ZIP64 pour les fichiers OOXML en Java."
type: docs
weight: 750
url: /fr/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

Spécifie quand utiliser les extensions de format ZIP64 pour les fichiers OOXML.

 **Remarks:** 

Le fichier OOXML est une archive ZIP qui possède une limite de 4 Go (2^32 octets) sur la taille non compressée d'un fichier, la taille compressée d'un fichier et la taille totale de l'archive, ainsi qu'une limite de 65 535 (2^16‑1) fichiers dans l'archive. Les extensions de format ZIP64 augmentent ces limites à 2^64.

 **Examples:** 

Montre comment utiliser les extensions de format ZIP64.

```

 Random random = new Random();
 DocumentBuilder builder = new DocumentBuilder();

 for (int i = 0; i < 10000; i++)
 {
     BufferedImage bmp = new BufferedImage(5, 5, BufferedImage.TYPE_INT_ARGB);
     Graphics2D g = bmp.createGraphics();
     g.setColor(new Color(random.nextInt(254), random.nextInt(254), random.nextInt(254)));
     g.drawImage(bmp, 0, 0, null);
     g.dispose();
     builder.insertImage(bmp);
 }

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setZip64Mode(Zip64Mode.ALWAYS);

 builder.getDocument().save(getArtifactsDir() + "OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ALWAYS](#ALWAYS) | Utilisez toujours les extensions de format ZIP64. |
| [IF_NECESSARY](#IF-NECESSARY) | Utilisez les extensions de format ZIP64 si nécessaire. |
| [NEVER](#NEVER) | N'utilisez pas les extensions de format ZIP64. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Utilisez toujours les extensions de format ZIP64.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


Utilisez les extensions de format ZIP64 si nécessaire.

### NEVER {#NEVER}
```
public static int NEVER
```


N'utilisez pas les extensions de format ZIP64.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zip64Mode) {#toString-int}
```
public static String toString(int zip64Mode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
