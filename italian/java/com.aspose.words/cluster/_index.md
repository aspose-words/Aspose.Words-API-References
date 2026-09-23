---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words per Java"
description: "Incapsula i punti di codice e i glifi che compongono un grafema in Java."
type: docs
weight: 104
url: /it/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Incapsula i punti di codice e i glifi che compongono un grafema.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [deepClone()](#deepClone) | Restituisce una copia profonda di questa istanza. |
| [getCodepoints()](#getCodepoints) | Ottiene i punti di codice del cluster. |
| [getCodepointsLength()](#getCodepointsLength) | Ottiene il numero totale di punti di codice nel [Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | Ottiene i glifi del cluster. |
| [getString()](#getString) | Crea java.lang.String utilizzando i punti di codice di questo cluster. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Crea java.lang.String utilizzando i punti di codice dei cluster specificati. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Restituisce la larghezza del cluster. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| codepoints | int[] | Array di punti Unicode che compongono un grafema. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Array di [Glyph](../../com.aspose.words/glyph/) > che compongono un grafema. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Restituisce una copia profonda di questa istanza.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Ottiene i punti di codice del cluster.

**Returns:**
int[] - Punti di codice del cluster.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


Ottiene il numero totale di punti di codice nel [Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - Numero totale di punti di codice nel [Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Ottiene i glifi del cluster.

**Returns:**
com.aspose.words.Glyph[] - Glifi del cluster.
### getString() {#getString}
```
public String getString()
```


Crea java.lang.String utilizzando i punti di codice di questo cluster.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Crea java.lang.String utilizzando i punti di codice dei cluster specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Restituisce la larghezza del cluster.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
