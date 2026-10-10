---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words für Java"
description: "Stellt Informationen über den aktuellen Produktnamen und die Version in Java bereit."
type: docs
weight: 51
url: /de/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Stellt Informationen über den aktuellen Produktnamen und die Version bereit.

Um mehr zu erfahren, besuchen Sie den [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie Informationen über Ihre installierte Version von Aspose.Words angezeigt werden.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getProduct()](#getProduct) | Ermittelt den vollständigen Namen des Produkts. |
| [getVersion()](#getVersion) | Ermittelt die Produktversion. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Ermittelt den vollständigen Namen des Produkts.

 **Examples:** 

Zeigt, wie Informationen über Ihre installierte Version von Aspose.Words angezeigt werden.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Der vollständige Name des Produkts.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Ermittelt die Produktversion.

 **Remarks:** 

Die Produktversion hat das Format "Major.Minor.Hotfix.0".

 **Examples:** 

Zeigt, wie Informationen über Ihre installierte Version von Aspose.Words angezeigt werden.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Die Produktversion.
