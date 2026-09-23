---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de configurer les options de césure du document en Java."
type: docs
weight: 388
url: /fr/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Permet de configurer les options de césure du document.

Pour en savoir plus, consultez l'article de documentation [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Obtient la valeur indiquant si la césure automatique est activée pour le document. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Obtient le nombre maximal de lignes consécutives pouvant se terminer par des tirets. |
| [getHyphenateCaps()](#getHyphenateCaps) | Obtient la valeur déterminant si les mots écrits en majuscules sont hyphénés. |
| [getHyphenationZone()](#getHyphenationZone) | Obtient la distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Définit la valeur déterminant si la césure automatique est activée pour le document. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Définit le nombre maximal de lignes consécutives pouvant se terminer par des tirets. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Définit la valeur déterminant si les mots écrits en majuscules sont hyphénés. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Définit la distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Obtient la valeur déterminant si la césure automatique est activée pour le document. La valeur par défaut de cette propriété est false.

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
booléen - Valeur déterminant si la césure automatique est activée pour le document.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Obtient le nombre maximal de lignes consécutives pouvant se terminer par des tirets. La valeur par défaut de cette propriété est 0.

 **Remarks:** 

Si la valeur de cette propriété est définie à 0, un nombre quelconque de lignes consécutives peut se terminer par des tirets.

La propriété n’a aucun effet lors de l’enregistrement aux formats de page fixe, par ex. PDF.

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - Le nombre maximal de lignes consécutives pouvant se terminer par des tirets.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Obtient la valeur déterminant si les mots écrits en majuscules sont hyphénés. La valeur par défaut de cette propriété est true.

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
booléen - Valeur déterminant si les mots écrits en majuscules sont hyphénés.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Obtient la distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce).

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - La distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Définit la valeur déterminant si la césure automatique est activée pour le document. La valeur par défaut de cette propriété est false.

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Valeur déterminant si la césure automatique est activée pour le document. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Définit le nombre maximal de lignes consécutives pouvant se terminer par des tirets. La valeur par défaut de cette propriété est 0.

 **Remarks:** 

Si la valeur de cette propriété est définie à 0, un nombre quelconque de lignes consécutives peut se terminer par des tirets.

La propriété n’a aucun effet lors de l’enregistrement aux formats de page fixe, par ex. PDF.

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le nombre maximal de lignes consécutives pouvant se terminer par des tirets. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Définit la valeur déterminant si les mots écrits en majuscules sont hyphénés. La valeur par défaut de cette propriété est true.

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Valeur déterminant si les mots écrits en majuscules sont hyphénés. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Définit la distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce).

 **Examples:** 

Montre comment configurer la césure automatique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. |

