---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words per Java"
description: "Specifica l'unità di misura per la larghezza preferita di una tabella o cella in Java."
type: docs
weight: 551
url: /it/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Specifica l'unità di misura per la larghezza preferita di una tabella o di una cella.

 **Examples:** 

Mostra come verificare il tipo e il valore della larghezza preferita di una cella di tabella.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | La larghezza preferita non è specificata. |
| [PERCENT](#PERCENT) | Misura la larghezza corrente dell'elemento usando una percentuale specificata. |
| [POINTS](#POINTS) | Misura la larghezza corrente dell'elemento usando un numero specificato di punti (1/72 di pollice). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


La larghezza preferita non è specificata. La larghezza effettiva della tabella o della cella è specificata tramite la larghezza esplicita oppure verrà determinata automaticamente dall'algoritmo di layout della tabella quando la tabella viene visualizzata, a seconda dell'impostazione di adattamento automatico della tabella.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Misura la larghezza corrente dell'elemento usando una percentuale specificata.

### POINTS {#POINTS}
```
public static int POINTS
```


Misura la larghezza corrente dell'elemento usando un numero specificato di punti (1/72 di pollice).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
