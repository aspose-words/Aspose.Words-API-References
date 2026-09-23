---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words für Java"
description: "Gibt Optionen für die Methode MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions in Java an."
type: docs
weight: 381
url: /de/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

Gibt Optionen für die Methode **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** an.

 **Examples:** 

Zeigt, wie man eine bessere Erhaltung von Rändern und Abständen ermöglicht.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [NONE](#NONE) | Verwenden Sie die Standardoptionen beim Einfügen von HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Eigenschaften von Block-Elementen erhalten. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Entfernen Sie den leeren Absatz, der normalerweise nach HTML eingefügt wird, das mit einem Block-Element endet. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | Verwenden Sie die in [DocumentBuilder](../../com.aspose.words/documentbuilder/) angegebene Schrift- und Absatzformatierung als Basisformatierung für aus HTML eingefügten Text. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int htmlInsertOptions)](#getName-int) |  |
| [getNames(int htmlInsertOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlInsertOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Verwenden Sie die Standardoptionen beim Einfügen von HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Eigenschaften von Block-Elementen erhalten.

 **Remarks:** 

Standardmäßig werden Eigenschaften von übergeordneten Blöcken zusammengeführt und auf ihren Kind-Elementen (d. h. Absätzen oder Tabellen) gespeichert. Wenn diese Option angegeben ist, werden die Eigenschaften jedes Blocks separat in einer speziellen logischen Struktur gespeichert. Dadurch ermöglicht diese Option, einzelne Rahmen und Ränder, die im HTML‑Dokument zu sehen sind, besser zu erhalten und bessere Konvertierungsergebnisse zu erzielen. Der Nachteil ist, dass das resultierende Dokument schwieriger zu bearbeiten ist, da in der logischen Struktur gespeicherte Rahmen und Ränder nicht zum Bearbeiten zur Verfügung stehen.

Nur Ränder und Rahmen der HTML‑Elemente 'body', 'div' und 'blockquote' werden erhalten. Die Eigenschaften jedes HTML‑Elements werden separat gespeichert.

Wenn diese Option angegeben ist, ahmt Aspose.Words das Verhalten von MS Word beim Import von Blockeigenschaften nach.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Entfernen Sie den leeren Absatz, der normalerweise nach HTML eingefügt wird, das mit einem Block-Element endet.

 **Remarks:** 

Standardmäßig stellt [DocumentBuilder](../../com.aspose.words/documentbuilder/) sicher, dass das zuletzt importierte Block‑Element aus HTML nach dem Import geschlossen wird und fügt nach dem Element einen Absatzumbruch ein. Dieser Absatzumbruch trennt den aus HTML importierten Inhalt vom Inhalt des Vorlagendokuments. Wird jedoch ein HTML‑Fragment in einen leeren Absatz eingefügt, erzeugt dieser Absatzumbruch einen zusätzlichen leeren Absatz. Wenn dieses Verhalten unerwünscht ist, geben Sie diese Option an.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


Verwenden Sie die in [DocumentBuilder](../../com.aspose.words/documentbuilder/) angegebene Schrift- und Absatzformatierung als Basisformatierung für aus HTML eingefügten Text.

 **Remarks:** 

Wenn diese Option nicht angegeben ist, wird die Formatierung von [DocumentBuilder](../../com.aspose.words/documentbuilder/) ignoriert und der Text mit der Standard‑HTML‑Formatierung eingefügt. Dadurch sieht der Text so aus, wie er in Browsern gerendert wird.

Wenn diese Option angegeben ist, basiert die Formatierung des eingefügten Textes auf der in [DocumentBuilder](../../com.aspose.words/documentbuilder/) angegebenen Formatierung, und der Text sieht so aus, als wäre er mit [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String) eingefügt worden.

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlInsertOptions) {#toString-int}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
