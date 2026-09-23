---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words для Java"
description: "Инкапсулирует кодовые точки и глифы, составляющие графему, в Java."
type: docs
weight: 104
url: /ru/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Инкапсулирует кодовые точки и глифы, составляющие графему.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Возвращает глубокую копию этого экземпляра. |
| [getCodepoints()](#getCodepoints) | Получает кодовые точки кластера. |
| [getCodepointsLength()](#getCodepointsLength) | Получает общее количество кодовых точек в [Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | Получает глифы кластера. |
| [getString()](#getString) | Создаёт java.lang.String, используя кодовые точки из этого кластера. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Создаёт java.lang.String, используя кодовые точки из указанных кластеров. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Возвращает ширину кластера. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| кодовые точки | int[] | Массив Unicode‑точек, составляющих графему. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Массив [Glyph](../../com.aspose.words/glyph/) >, составляющих графему. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Возвращает глубокую копию этого экземпляра.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Получает кодовые точки кластера.

**Returns:**
int[] - Кодовые точки кластера.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


Получает общее количество кодовых точек в [Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - Общее количество кодовых точек в [Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Получает глифы кластера.

**Returns:**
com.aspose.words.Glyph[] - Глифы кластера.
### getString() {#getString}
```
public String getString()
```


Создаёт java.lang.String, используя кодовые точки из этого кластера.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Создаёт java.lang.String, используя кодовые точки из указанных кластеров.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Возвращает ширину кластера.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
