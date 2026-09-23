---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words per Java"
description: "Specifica la regola per determinare l'altezza di un oggetto in Java."
type: docs
weight: 373
url: /it/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Specifica la regola per determinare l'altezza di un oggetto.

 **Examples:** 

Mostra come formattare le righe con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | L'altezza sarà almeno l'altezza specificata in punti. |
| [AUTO](#AUTO) | L'altezza crescerà automaticamente per contenere tutto il testo all'interno di un oggetto. |
| [EXACTLY](#EXACTLY) | L'altezza è specificata esattamente in punti. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


L'altezza sarà almeno l'altezza specificata in punti. Crescerà, se necessario, per contenere tutto il testo all'interno di un oggetto.

### AUTO {#AUTO}
```
public static int AUTO
```


L'altezza crescerà automaticamente per contenere tutto il testo all'interno di un oggetto.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


L'altezza è specificata esattamente in punti. Si prega di notare che se il testo non può entrare nell'oggetto di questa altezza, verrà troncato.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
