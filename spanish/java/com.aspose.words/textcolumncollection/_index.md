---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de objetos TextColumn que representan todas las columnas de texto en una sección de un documento en Java."
type: docs
weight: 671
url: /es/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

Una colección de [TextColumn](../../com.aspose.words/textcolumn/) objetos que representan todas las columnas de texto en una sección de un documento.

Para obtener más información, visite el artículo de documentación [ Working with Sections ][Working with Sections].

 **Remarks:** 

Utilice [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) para establecer el número de columnas de texto.

Para que todas las columnas tengan el mismo ancho y estén espaciadas uniformemente, establezca [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) en true y especifique la cantidad de espacio entre las columnas en [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double). MS Word calculará automáticamente el ancho de las columnas.

Si tiene [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) configurado en false, necesita especificar el ancho y el espaciado para cada columna individualmente. Utilice el indexador para acceder a los objetos [TextColumn](../../com.aspose.words/textcolumn/) individuales.

Al usar anchos de columna personalizados, asegúrese de que la suma de todos los anchos de columna y los espaciados entre ellos sea igual al ancho de página menos los márgenes izquierdo y derecho.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Devuelve una columna de texto en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de columnas en la sección de un documento. |
| [getEvenlySpaced()](#getEvenlySpaced) | True si las columnas de texto tienen el mismo ancho y están espaciadas uniformemente. |
| [getLineBetween()](#getLineBetween) | Cuando true, agrega una línea vertical entre las columnas. |
| [getSpacing()](#getSpacing) | Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos. |
| [getWidth()](#getWidth) | Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas. |
| [setCount(int newCount)](#setCount-int) | Organiza el texto en el número especificado de columnas de texto. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | True si las columnas de texto tienen el mismo ancho y están espaciadas uniformemente. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | Cuando true, agrega una línea vertical entre las columnas. |
| [setSpacing(double value)](#setSpacing-double) | Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Devuelve una columna de texto en el índice especificado.

 **Examples:** 

Muestra cómo crear columnas con espaciado desigual.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de columnas en la sección de un documento.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
int - El número de columnas en la sección de un documento.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


True si las columnas de texto tienen el mismo ancho y están espaciadas uniformemente.

 **Examples:** 

Muestra cómo crear columnas con espaciado desigual.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


Cuando true, agrega una línea vertical entre las columnas.

 **Examples:** 

Muestra cómo separar columnas con una línea vertical.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos.

 **Remarks:** 

Tiene efecto solo cuando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) está configurado en true.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - El valor  double  correspondiente.
### getWidth() {#getWidth}
```
public double getWidth()
```


Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas.

 **Remarks:** 

Tiene efecto solo cuando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) está configurado en true.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - El valor  double  correspondiente.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Organiza el texto en el número especificado de columnas de texto.

 **Remarks:** 

Cuando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) está en false y aumenta el número de columnas, se crean nuevos objetos [TextColumn](../../com.aspose.words/textcolumn/) con ancho y espaciado cero. Necesita establecer el ancho y el espaciado para las nuevas columnas.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| newCount | int | El número de columnas en las que se organizará el texto. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


True si las columnas de texto tienen el mismo ancho y están espaciadas uniformemente.

 **Examples:** 

Muestra cómo crear columnas con espaciado desigual.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


Cuando true, agrega una línea vertical entre las columnas.

 **Examples:** 

Muestra cómo separar columnas con una línea vertical.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos.

 **Remarks:** 

Tiene efecto solo cuando [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) está configurado en true.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor  double  correspondiente. |

