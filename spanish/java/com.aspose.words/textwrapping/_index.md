---
title: "TextWrapping"
linktitle: "TextWrapping"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se ajusta el texto alrededor de la tabla en Java."
type: docs
weight: 679
url: /es/java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

Especifica cómo se ajusta el texto alrededor de la tabla.

 **Examples:** 

Muestra cómo trabajar con el ajuste de texto de la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AROUND](#AROUND) | El texto se ajusta alrededor de la tabla ocupando el espacio lateral disponible. |
| [DEFAULT](#DEFAULT) | Valor predeterminado. |
| [NONE](#NONE) | El texto y la tabla se muestran en el orden de su aparición en el documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textWrapping)](#toString-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


El texto se ajusta alrededor de la tabla ocupando el espacio lateral disponible.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Valor predeterminado.

### NONE {#NONE}
```
public static int NONE
```


El texto y la tabla se muestran en el orden de su aparición en el documento.

### length {#length}
```
public static int length
```


### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textWrapping) {#toString-int}
```
public static String toString(int textWrapping)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
