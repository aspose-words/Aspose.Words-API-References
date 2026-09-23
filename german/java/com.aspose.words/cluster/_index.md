---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words für Java"
description: "Kapselt Codepunkte und Glyphen, die ein Graphem in Java bilden."
type: docs
weight: 104
url: /de/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Kapselt Codepunkte und Glyphen, die ein Graphem bilden.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Gibt eine tiefe Kopie dieser Instanz zurück. |
| [getCodepoints()](#getCodepoints) | Liefert die Codepunkte des Clusters. |
| [getCodepointsLength()](#getCodepointsLength) | Liefert die Gesamtzahl der Codepunkte im [Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | Liefert die Glyphen des Clusters. |
| [getString()](#getString) | Erstellt java.lang.String unter Verwendung von Codepunkten aus diesem Cluster. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Erstellt java.lang.String unter Verwendung von Codepunkten aus den angegebenen Clustern. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Gibt die Breite des Clusters zurück. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| codepoints | int[] | Array von Unicode-Punkten, die ein Graphem bilden. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Array von [Glyph](../../com.aspose.words/glyph/) > zur Zusammensetzung eines Graphems. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Gibt eine tiefe Kopie dieser Instanz zurück.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Liefert die Codepunkte des Clusters.

**Returns:**
int[] - Codepunkte des Clusters.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


Liefert die Gesamtzahl der Codepunkte im [Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - Gesamtzahl der Codepunkte im [Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Liefert die Glyphen des Clusters.

**Returns:**
com.aspose.words.Glyph[] - Glyphs des Clusters.
### getString() {#getString}
```
public String getString()
```


Erstellt java.lang.String unter Verwendung von Codepunkten aus diesem Cluster.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Erstellt java.lang.String unter Verwendung von Codepunkten aus den angegebenen Clustern.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Gibt die Breite des Clusters zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
