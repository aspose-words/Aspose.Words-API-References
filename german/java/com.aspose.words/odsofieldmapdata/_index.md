---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie eine Spalte in der externen Datenquelle auf die vordefinierten Merge-Felder im Dokument in Java abgebildet werden soll."
type: docs
weight: 489
url: /de/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Gibt an, wie eine Spalte in der externen Datenquelle den vordefinierten Seriendruckfeldern im Dokument zugeordnet wird.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Microsoft Word stellt einige vordefinierte Seriendruckfeldnamen bereit, die es ermöglicht, sie in ein Dokument als MERGEFIELD einzufügen oder in den Feldern ADDRESSBLOCK oder GREETINGLINE zu verwenden. Die in [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) angegebenen Informationen ermöglichen es, eine Spalte in der externen Datenquelle einer einzelnen vordefinierten Seriendruckfeld zuzuordnen.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [getColumn()](#getColumn) | Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Feldes zugeordnet werden soll. |
| [getMappedName()](#getMappedName) | Gibt den vordefinierten Seriendruckfeldnamen an, der der Spaltennummer zugeordnet werden soll, die durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) in dieser Feldzuordnung angegeben ist. |
| [getName()](#getName) | Gibt den Spaltennamen in einer externen Datenquelle für die Spalte an, deren Index durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) festgelegt ist. |
| [getType()](#getType) | Gibt an, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. |
| [setColumn(int value)](#setColumn-int) | Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Feldes zugeordnet werden soll. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Gibt den vordefinierten Seriendruckfeldnamen an, der der Spaltennummer zugeordnet werden soll, die durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) in dieser Feldzuordnung angegeben ist. |
| [setName(String value)](#setName-java.lang.String) | Gibt den Spaltennamen in einer externen Datenquelle für die Spalte an, deren Index durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) festgelegt ist. |
| [setType(int value)](#setType-int) | Gibt an, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Gibt eine tiefe Kopie dieses Objekts zurück.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Feldes zugeordnet werden soll. Der Standardwert ist 0.

**Returns:**
int - Der entsprechende int-Wert.
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Gibt den vordefinierten Seriendruckfeldnamen an, der der Spaltennummer zugeordnet werden soll, die durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) in dieser Feldzuordnung angegeben ist. Der Standardwert ist ein leerer String.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getName() {#getName}
```
public String getName()
```


Gibt den Spaltennamen in einer externen Datenquelle für die Spalte an, deren Index durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) festgelegt ist. Der Standardwert ist ein leerer String.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getType() {#getType}
```
public int getType()
```


Gibt an, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. Der Standardwert ist [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/#DEFAULT).

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/) .
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Feldes zugeordnet werden soll. Der Standardwert ist 0.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Gibt den vordefinierten Seriendruckfeldnamen an, der der Spaltennummer zugeordnet werden soll, die durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) in dieser Feldzuordnung angegeben ist. Der Standardwert ist ein leerer String.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Gibt den Spaltennamen in einer externen Datenquelle für die Spalte an, deren Index durch die Eigenschaft [getColumn()](../../com.aspose.words/odsofieldmapdata/#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/#setColumn-int) festgelegt ist. Der Standardwert ist ein leerer String.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Gibt an, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. Der Standardwert ist [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/#DEFAULT).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/) sein. |

