---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words para Java"
description: "Encapsula puntos de código y glifos que componen un grafema en Java."
type: docs
weight: 104
url: /es/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Encapsula puntos de código y glifos que componen un grafema.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [deepClone()](#deepClone) | Devuelve una clonación profunda de esta instancia. |
| [getCodepoints()](#getCodepoints) | Obtiene los puntos de código del clúster. |
| [getCodepointsLength()](#getCodepointsLength) | Obtiene el número total de puntos de código en el [Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | Obtiene los glifos del clúster. |
| [getString()](#getString) | Crea java.lang.String usando puntos de código de este clúster. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Crea java.lang.String usando puntos de código de los clústeres especificados. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Devuelve el ancho del clúster. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| puntos de código | int[] | Arreglo de puntos Unicode que componen un grafema. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Arreglo de [Glyph](../../com.aspose.words/glyph/) > que componen un grafema. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Devuelve una clonación profunda de esta instancia.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Obtiene los puntos de código del clúster.

**Returns:**
int[] - Puntos de código del clúster.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


Obtiene el número total de puntos de código en el [Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - Número total de puntos de código en el [Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Obtiene los glifos del clúster.

**Returns:**
com.aspose.words.Glyph[] - Glifos del clúster.
### getString() {#getString}
```
public String getString()
```


Crea java.lang.String usando puntos de código de este clúster.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Crea java.lang.String usando puntos de código de los clústeres especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Devuelve el ancho del clúster.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
