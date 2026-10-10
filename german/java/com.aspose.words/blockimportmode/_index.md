---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Eigenschaften von Block‑Elementen aus HTML‑basierten Dokumenten in Java importiert werden."
type: docs
weight: 39
url: /de/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Gibt an, wie Eigenschaften von Block‑Elementen aus HTML‑basierten Dokumenten importiert werden.

 **Examples:** 

Zeigt, wie Eigenschaften von Block‑Elementen aus HTML‑basierten Dokumenten importiert werden.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [MERGE](#MERGE) | Eigenschaften von übergeordneten Blöcken werden zusammengeführt und auf Kind‑Elementen gespeichert (z. B. |
| [PRESERVE](#PRESERVE) | Eigenschaften von übergeordneten Blöcken werden in eine spezielle logische Struktur importiert und getrennt von Dokumentknoten gespeichert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Eigenschaften von übergeordneten Blöcken werden zusammengeführt und auf Kind‑Elementen gespeichert (z. B. Absätze oder Tabellen).

 **Remarks:** 

Eigenschaften von übergeordneten Blöcken werden wie folgt zusammengeführt: Ränder werden addiert; Rahmen höherer Ebenen werden verworfen und nur die innersten Rahmen erhalten bleiben. Infolgedessen gehen bei Angabe dieses Modus einige Formatierungen der Blöcke aus dem Originaldokument verloren.

Andererseits, da alle zusammengeführten Block‑Eigenschaften auf Dokumentknoten gespeichert werden, ist die gesamte Formatierung im resultierenden Dokument zur Bearbeitung verfügbar.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Eigenschaften von übergeordneten Blöcken werden in eine spezielle logische Struktur importiert und getrennt von Dokumentknoten gespeichert.

 **Remarks:** 

Nur Ränder und Rahmen der HTML‑Elemente 'body', 'div' und 'blockquote' werden importiert. Eigenschaften jedes HTML‑Elements werden einzeln gespeichert.

Dieser Modus ermöglicht es, Rahmen und Ränder des HTML‑Dokuments besser zu erhalten und bessere Konvertierungsergebnisse zu erzielen. Der Nachteil ist, dass das resultierende Dokument schwerer zu bearbeiten ist, da in der logischen Struktur gespeicherte Rahmen und Ränder nicht editierbar sind.

Dieser Modus ahmt das Verhalten von MS Word beim Import von Block‑Eigenschaften nach.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
