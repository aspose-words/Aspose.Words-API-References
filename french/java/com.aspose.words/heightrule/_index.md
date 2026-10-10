---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words pour Java"
description: "Spécifie la règle de détermination de la hauteur d'un objet en Java."
type: docs
weight: 373
url: /fr/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Spécifie la règle de détermination de la hauteur d’un objet.

 **Examples:** 

Montre comment formater les lignes avec un document builder.

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
## Champs

| Champ | Description |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | La hauteur sera au moins la hauteur spécifiée en points. |
| [AUTO](#AUTO) | La hauteur augmentera automatiquement pour accueillir tout le texte à l'intérieur d'un objet. |
| [EXACTLY](#EXACTLY) | La hauteur est spécifiée exactement en points. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


La hauteur sera au moins la hauteur spécifiée en points. Elle augmentera, si nécessaire, pour accueillir tout le texte à l'intérieur d'un objet.

### AUTO {#AUTO}
```
public static int AUTO
```


La hauteur augmentera automatiquement pour accueillir tout le texte à l'intérieur d'un objet.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


La hauteur est spécifiée exactement en points. Veuillez noter que si le texte ne peut pas tenir dans l'objet de cette hauteur, il sera tronqué.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
