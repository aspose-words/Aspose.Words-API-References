---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Konfigurieren von Silbentrennungsoptionen für Dokumente in Java."
type: docs
weight: 388
url: /de/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Ermöglicht die Konfiguration von Silbentrennungsoptionen für das Dokument.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Ermittelt den Wert, der festlegt, ob die automatische Silbentrennung für das Dokument aktiviert ist. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Ermittelt die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können. |
| [getHyphenateCaps()](#getHyphenateCaps) | Ermittelt den Wert, der festlegt, ob Wörter, die komplett in Großbuchstaben geschrieben sind, getrennt werden. |
| [getHyphenationZone()](#getHyphenationZone) | Ermittelt den Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Legt den Wert fest, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Legt die maximale Anzahl aufeinanderfolgender Zeilen fest, die mit Bindestrichen enden können. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Legt den Wert fest, der bestimmt, ob Wörter, die komplett in Großbuchstaben geschrieben sind, getrennt werden. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Legt den Abstand in 1/20 Punkt vom rechten Rand fest, innerhalb dessen Wörter nicht getrennt werden sollen. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Ermittelt den Wert, der festlegt, ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft ist  false .

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
boolean - Wert, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Ermittelt die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können. Der Standardwert für diese Eigenschaft ist 0.

 **Remarks:** 

Wenn der Wert dieser Eigenschaft auf 0 gesetzt ist, kann eine beliebige Anzahl aufeinanderfolgender Zeilen mit Bindestrichen enden.

Die Eigenschaft hat keinen Effekt beim Speichern in feste Seitenformate, z. B. PDF.

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
int - Die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Ermittelt den Wert, der bestimmt, ob in Großbuchstaben geschriebene Wörter getrennt werden. Der Standardwert für diese Eigenschaft ist true.

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
boolean - Wert, der bestimmt, ob in Großbuchstaben geschriebene Wörter getrennt werden.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Ermittelt den Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll).

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
int - Der Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Legt den Wert fest, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft ist false.

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Wert, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Legt die maximale Anzahl aufeinanderfolgender Zeilen fest, die mit Bindestrichen enden können. Der Standardwert für diese Eigenschaft ist 0.

 **Remarks:** 

Wenn der Wert dieser Eigenschaft auf 0 gesetzt ist, kann eine beliebige Anzahl aufeinanderfolgender Zeilen mit Bindestrichen enden.

Die Eigenschaft hat keinen Effekt beim Speichern in feste Seitenformate, z. B. PDF.

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Legt den Wert fest, der bestimmt, ob in Großbuchstaben geschriebene Wörter getrennt werden. Der Standardwert für diese Eigenschaft ist true.

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Wert, der bestimmt, ob in Großbuchstaben geschriebene Wörter getrennt werden. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Legt den Abstand in 1/20 Punkt vom rechten Rand fest, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll).

 **Examples:** 

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Abstand in 1/20 Punkt vom rechten Rand, innerhalb dessen Wörter nicht getrennt werden sollen. |

