---
title: "TableStyle"
linktitle: "TableStyle"
second_title: "Aspose.Words para Java"
description: "Representa un estilo de tabla en Java."
type: docs
weight: 660
url: /es/java/com.aspose.words/tablestyle/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Style](../../com.aspose.words/style/)
```
public class TableStyle extends Style
```

Representa un estilo de tabla.

Para obtener más información, visite el artículo de documentación [ Working with Tables ][Working with Tables].

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | Compara con el estilo especificado. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAliases()](#getAliases) | Obtiene todos los alias de este estilo. |
| [getAlignment()](#getAlignment) | Especifica la alineación para el estilo de tabla. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages) | Obtiene una bandera que indica si el texto en una fila de tabla puede dividirse al cruzar un salto de página. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | Especifica si este estilo se redefine automáticamente según el valor apropiado. |
| [getBaseStyleName()](#getBaseStyleName) | Obtiene/establece el nombre del estilo del cual se basa este estilo. |
| [getBorders()](#getBorders) | Obtiene la colección de bordes de celda predeterminados para el estilo. |
| [getBottomPadding()](#getBottomPadding) | Obtiene la cantidad de espacio (en puntos) que se añade debajo del contenido de las celdas de la tabla. |
| [getBuiltIn()](#getBuiltIn) | Verdadero si este estilo es uno de los estilos incorporados en MS Word. |
| [getCellSpacing()](#getCellSpacing) | Obtiene la cantidad de espacio (en puntos) entre las celdas. |
| [getColumnStripe()](#getColumnStripe) | Obtiene un número de columnas que se incluirán en la banda cuando el estilo especifica bandas de columnas impares/pares. |
| [getConditionalStyles()](#getConditionalStyles) | Colección de estilos condicionales que pueden definirse para este estilo de tabla. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Obtiene el documento propietario. |
| [getFont()](#getFont) | Obtiene el formato de carácter del estilo. |
| [getLeftIndent()](#getLeftIndent) | Obtiene el valor que representa la sangría izquierda de una tabla. |
| [getLeftPadding()](#getLeftPadding) | Obtiene la cantidad de espacio (en puntos) que se añade a la izquierda del contenido de las celdas de la tabla. |
| [getLinkedStyleName()](#getLinkedStyleName) | Obtiene/establece el nombre del [Style](../../com.aspose.words/style/) vinculado a este. |
| [getList()](#getList) | Obtiene la lista que define el formato de este estilo de lista. |
| [getListFormat()](#getListFormat) | Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo. |
| [getLocked()](#getLocked) | Especifica si este estilo está bloqueado. |
| [getName()](#getName) | Obtiene el nombre del estilo. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado. |
| [getParagraphFormat()](#getParagraphFormat) | Obtiene el formato de párrafo del estilo. |
| [getPriority()](#getPriority) | Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas Estilos. |
| [getRightPadding()](#getRightPadding) | Obtiene la cantidad de espacio (en puntos) que se añade a la derecha del contenido de las celdas de la tabla. |
| [getRowStripe()](#getRowStripe) | Obtiene un número de filas que se incluirán en la banda cuando el estilo especifica bandas de filas impares/pares. |
| [getSemiHidden()](#getSemiHidden) | Obtiene/establece si el estilo se oculta de la galería Estilos y del panel de tareas Estilos. |
| [getShading()](#getShading) | Obtiene un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado para las celdas de tabla. |
| [getStyleIdentifier()](#getStyleIdentifier) | Obtiene el identificador de estilo independiente de la configuración regional para un estilo incorporado. |
| [getStyles()](#getStyles) | Obtiene la colección de estilos a los que pertenece este estilo. |
| [getTopPadding()](#getTopPadding) | Obtiene la cantidad de espacio (en puntos) que se añade encima del contenido de las celdas de la tabla. |
| [getType()](#getType) | Obtiene el tipo de estilo (párrafo o carácter). |
| [getUnhideWhenUsed()](#getUnhideWhenUsed) | Obtiene/establece si el estilo usado en el documento actual se muestra nuevamente en la galería Estilos y en el panel de tareas Estilos. |
| [getVerticalAlignment()](#getVerticalAlignment) | Especifica la alineación vertical para las celdas. |
| [isHeading()](#isHeading) | Verdadero cuando el estilo es uno de los estilos de encabezado incorporados. |
| [isQuickStyle()](#isQuickStyle) | Especifica si este estilo se muestra en la galería de Estilos rápidos dentro de la interfaz de MS Word. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | Especifica si este estilo se muestra en la galería de Estilos rápidos dentro de la interfaz de MS Word. |
| [remove()](#remove) | Elimina el estilo especificado del documento. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setAlignment(int value)](#setAlignment-int) | Especifica la alineación para el estilo de tabla. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean) | Establece una bandera que indica si el texto en una fila de tabla puede dividirse al cruzar un salto de página. |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | Especifica si este estilo se redefine automáticamente según el valor apropiado. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | Obtiene/establece el nombre del estilo del cual se basa este estilo. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Establece la cantidad de espacio (en puntos) que se añade debajo del contenido de las celdas de la tabla. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setCellSpacing(double value)](#setCellSpacing-double) | Establece la cantidad de espacio (en puntos) entre las celdas. |
| [setColumnStripe(int value)](#setColumnStripe-int) | Establece un número de columnas que se incluirán en la banda cuando el estilo especifica bandas de columnas impares/pares. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Establece el valor que representa la sangría izquierda de una tabla. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Establece la cantidad de espacio (en puntos) que se añade a la izquierda del contenido de las celdas de la tabla. |
| [setLinkedStyleName(String value)](#setLinkedStyleName-java.lang.String) | Obtiene/establece el nombre del [Style](../../com.aspose.words/style/) vinculado a este. |
| [setLocked(boolean value)](#setLocked-boolean) | Especifica si este estilo está bloqueado. |
| [setName(String value)](#setName-java.lang.String) | Establece el nombre del estilo. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setPriority(int value)](#setPriority-int) | Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas Estilos. |
| [setRightPadding(double value)](#setRightPadding-double) | Establece la cantidad de espacio (en puntos) que se añade a la derecha del contenido de las celdas de la tabla. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRowStripe(int value)](#setRowStripe-int) | Establece un número de filas que se incluirán en la banda cuando el estilo especifica bandas de filas impares/pares. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setSemiHidden(boolean value)](#setSemiHidden-boolean) | Obtiene/establece si el estilo se oculta de la galería Estilos y del panel de tareas Estilos. |
| [setTopPadding(double value)](#setTopPadding-double) | Establece la cantidad de espacio (en puntos) que se añade encima del contenido de las celdas de la tabla. |
| [setUnhideWhenUsed(boolean value)](#setUnhideWhenUsed-boolean) | Obtiene/establece si el estilo usado en el documento actual se muestra nuevamente en la galería Estilos y en el panel de tareas Estilos. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Especifica la alineación vertical para las celdas. |
### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


Compara con el estilo especificado. Los Istds de estilos se comparan solo para estilos incorporados. Los valores predeterminados de estilos no se incluyen en la comparación. El estilo base, el estilo vinculado y el estilo de siguiente párrafo se comparan recursivamente.

 **Examples:** 

Muestra cómo usar alias de estilo.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


Obtiene todos los alias de este estilo. Si el estilo no tiene alias, se devuelve una matriz vacía de cadenas.

 **Examples:** 

Muestra cómo usar alias de estilo.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String[] - Todos los alias de este estilo.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Especifica la alineación para el estilo de tabla.

 **Remarks:** 

El valor predeterminado es [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

Muestra cómo establecer la posición de una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes de [TableAlignment](../../com.aspose.words/tablealignment/).
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages}
```
public boolean getAllowBreakAcrossPages()
```


Obtiene una bandera que indica si el texto en una fila de tabla puede dividirse al cruzar un salto de página.

 **Remarks:** 

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
boolean - Una bandera que indica si el texto en una fila de tabla puede dividirse al cruzar un salto de página.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


Especifica si este estilo se redefine automáticamente según el valor apropiado.

 **Remarks:** 

Si el valor de la propiedad se establece en verdadero, MS Word redefine automáticamente el estilo actual cuando se ha cambiado el formato de párrafo correspondiente.

La propiedad AutomaticallyUpdate solo se aplica a estilos de párrafo.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo crear y aplicar un estilo personalizado.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


Obtiene/establece el nombre del estilo del cual se basa este estilo.

 **Remarks:** 

Esto será una cadena vacía si el estilo no se basa en ningún otro estilo y puede establecerse como una cadena vacía.

 **Examples:** 

Muestra cómo usar alias de estilo.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Obtiene la colección de bordes de celda predeterminados para el estilo.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of default cell borders for the style.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añade debajo del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se añade debajo del contenido de las celdas de la tabla.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


Verdadero si este estilo es uno de los estilos incorporados en MS Word.

 **Examples:** 

Muestra cómo diferenciar estilos personalizados de los estilos incorporados.

```

 Document doc = new Document();

 // When we create a document using Microsoft Word, or programmatically using Aspose.Words,
 // the document will come with a collection of styles to apply to its text to modify its appearance.
 // We can access these built-in styles via the document's "Styles" collection.
 // These styles will all have the "BuiltIn" flag set to "true".
 Style style = doc.getStyles().get("Emphasis");

 Assert.assertTrue(style.getBuiltIn());

 // Create a custom style and add it to the collection.
 // Custom styles such as this will have the "BuiltIn" flag set to "false".
 style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 Assert.assertFalse(style.getBuiltIn());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getCellSpacing() {#getCellSpacing}
```
public double getCellSpacing()
```


Obtiene la cantidad de espacio (en puntos) entre las celdas.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) entre las celdas.
### getColumnStripe() {#getColumnStripe}
```
public int getColumnStripe()
```


Obtiene un número de columnas que se incluirán en la banda cuando el estilo especifica bandas de columnas impares/pares.

 **Examples:** 

Muestra cómo crear estilos de tabla condicionales que alternan entre filas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - Un número de columnas que se incluirán en la banda cuando el estilo especifica bandas de columnas impares/pares.
### getConditionalStyles() {#getConditionalStyles}
```
public ConditionalStyleCollection getConditionalStyles()
```


Colección de estilos condicionales que pueden definirse para este estilo de tabla.

 **Examples:** 

Muestra cómo trabajar con ciertos estilos de área de una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) - The corresponding [ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Obtiene el documento propietario.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


Obtiene el formato de carácter del estilo.

 **Remarks:** 

Para estilos de lista, esta propiedad devuelve  null .

 **Examples:** 

Muestra cómo crear y aplicar un estilo personalizado.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

Muestra cómo crear y usar un estilo de párrafo con formato de lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Obtiene el valor que representa la sangría izquierda de una tabla.

 **Examples:** 

Muestra cómo establecer la posición de una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
double - El valor que representa la sangría izquierda de una tabla.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añade a la izquierda del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se añade a la izquierda del contenido de las celdas de la tabla.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


Obtiene/establece el nombre del [Style](../../com.aspose.words/style/) vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados.

 **Remarks:** 

Solo se permite vincular el estilo de párrafo al estilo de carácter y viceversa.

Establecer LinkedStyleName para el estilo actual lleva automáticamente a establecer LinkedStyleName para el estilo vinculado.

Asignar una cadena vacía equivale a desvincular el estilo previamente vinculado.

 **Examples:** 

Muestra cómo usar alias de estilo.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Muestra cómo vincular estilos entre sí.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getList() {#getList}
```
public List getList()
```


Obtiene la lista que define el formato de este estilo de lista.

 **Remarks:** 

Esta propiedad solo es válida para estilos de lista. Para otros tipos de estilo, esta propiedad devuelve  null .

 **Examples:** 

Muestra cómo crear un estilo de lista y usarlo en un documento.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo.

 **Remarks:** 

Esta propiedad solo es válida para estilos de párrafo. Para otros tipos de estilo, esta propiedad devuelve  null .

 **Examples:** 

Muestra cómo crear y usar un estilo de párrafo con formato de lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getLocked() {#getLocked}
```
public boolean getLocked()
```


Especifica si este estilo está bloqueado.

 **Examples:** 

Muestra cómo bloquear un estilo.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getName() {#getName}
```
public String getName()
```


Obtiene el nombre del estilo.

 **Remarks:** 

No puede ser una cadena vacía.

Si ya existe un estilo con ese nombre en la colección, este estilo lo sobrescribirá. Todos los nodos afectados harán referencia al nuevo estilo.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - El nombre del estilo.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado.

 **Remarks:** 

Esta propiedad no es utilizada por Aspose.Words. El siguiente estilo de párrafo solo se aplicará automáticamente cuando edite el documento en MS Word.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Obtiene el formato de párrafo del estilo.

 **Remarks:** 

Para estilos de carácter y de lista, esta propiedad devuelve  null .

 **Examples:** 

Muestra cómo crear y usar un estilo de párrafo con formato de lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getPriority() {#getPriority}
```
public int getPriority()
```


Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas Estilos.

 **Examples:** 

Muestra cómo priorizar y ocultar un estilo.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
int - El valor  int  correspondiente.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añade a la derecha del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se añade a la derecha del contenido de las celdas de la tabla.
### getRowStripe() {#getRowStripe}
```
public int getRowStripe()
```


Obtiene un número de filas que se incluirán en la banda cuando el estilo especifica bandas de filas impares/pares.

 **Examples:** 

Muestra cómo crear estilos de tabla condicionales que alternan entre filas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - Un número de filas que se incluirán en la banda cuando el estilo especifica bandas de filas impares/pares.
### getSemiHidden() {#getSemiHidden}
```
public boolean getSemiHidden()
```


Obtiene/establece si el estilo se oculta de la galería Estilos y del panel de tareas Estilos.

 **Examples:** 

Muestra cómo priorizar y ocultar un estilo.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getShading() {#getShading}
```
public Shading getShading()
```


Obtiene un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado para las celdas de tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Obtiene el identificador de estilo independiente de la configuración regional para un estilo incorporado.

 **Remarks:** 

Para estilos definidos por el usuario (personalizados), esta propiedad devuelve [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\#USER).

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - El identificador de estilo independiente de la configuración regional para un estilo incorporado. El valor devuelto es una de las constantes de [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Obtiene la colección de estilos a los que pertenece este estilo.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añade encima del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se añade encima del contenido de las celdas de la tabla.
### getType() {#getType}
```
public int getType()
```


Obtiene el tipo de estilo (párrafo o carácter).

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
int - El tipo de estilo (párrafo o carácter). El valor devuelto es una de las constantes de [StyleType](../../com.aspose.words/styletype/).
### getUnhideWhenUsed() {#getUnhideWhenUsed}
```
public boolean getUnhideWhenUsed()
```


Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas de Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos.

 **Examples:** 

Muestra cómo priorizar y ocultar un estilo.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Especifica la alineación vertical para las celdas.

 **Remarks:** 

El valor predeterminado es [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/\#TOP).

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/).
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Verdadero cuando el estilo es uno de los estilos de encabezado incorporados.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


Especifica si este estilo se muestra en la galería de Estilos rápidos dentro de la interfaz de MS Word.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


Especifica si este estilo se muestra en la galería de Estilos rápidos dentro de la interfaz de MS Word.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### remove() {#remove}
```
public void remove()
```


Elimina el estilo especificado del documento.

 **Remarks:** 

La eliminación de estilos tiene los siguientes efectos en el modelo de documento:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

 **Examples:** 

Muestra cómo crear y aplicar un estilo personalizado.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Especifica la alineación para el estilo de tabla.

 **Remarks:** 

El valor predeterminado es [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

Muestra cómo establecer la posición de una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes de [TableAlignment](../../com.aspose.words/tablealignment/). |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean}
```
public void setAllowBreakAcrossPages(boolean value)
```


Establece una bandera que indica si el texto en una fila de tabla puede dividirse al cruzar un salto de página.

 **Remarks:** 

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si el texto en una fila de tabla puede dividirse en un salto de página. |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


Especifica si este estilo se redefine automáticamente según el valor apropiado.

 **Remarks:** 

Si el valor de la propiedad se establece en verdadero, MS Word redefine automáticamente el estilo actual cuando se ha cambiado el formato de párrafo correspondiente.

La propiedad AutomaticallyUpdate solo se aplica a estilos de párrafo.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo crear y aplicar un estilo personalizado.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


Obtiene/establece el nombre del estilo del cual se basa este estilo.

 **Remarks:** 

Esto será una cadena vacía si el estilo no se basa en ningún otro estilo y puede establecerse como una cadena vacía.

 **Examples:** 

Muestra cómo usar alias de estilo.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añade debajo del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir debajo del contenido de las celdas de la tabla. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double}
```
public void setCellSpacing(double value)
```


Establece la cantidad de espacio (en puntos) entre las celdas.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) entre las celdas. |

### setColumnStripe(int value) {#setColumnStripe-int}
```
public void setColumnStripe(int value)
```


Establece un número de columnas que se incluirán en la banda cuando el estilo especifica bandas de columnas impares/pares.

 **Examples:** 

Muestra cómo crear estilos de tabla condicionales que alternan entre filas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | Un número de columnas a incluir en el sombreado cuando el estilo especifica sombreado de columnas impares/pares. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Establece el valor que representa la sangría izquierda de una tabla.

 **Examples:** 

Muestra cómo establecer la posición de una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor que representa la sangría izquierda de una tabla. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añade a la izquierda del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir a la izquierda del contenido de las celdas de la tabla. |

### setLinkedStyleName(String value) {#setLinkedStyleName-java.lang.String}
```
public void setLinkedStyleName(String value)
```


Obtiene/establece el nombre del [Style](../../com.aspose.words/style/) vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados.

 **Remarks:** 

Solo se permite vincular el estilo de párrafo al estilo de carácter y viceversa.

Establecer LinkedStyleName para el estilo actual lleva automáticamente a establecer LinkedStyleName para el estilo vinculado.

Asignar una cadena vacía equivale a desvincular el estilo previamente vinculado.

 **Examples:** 

Muestra cómo usar alias de estilo.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Muestra cómo vincular estilos entre sí.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setLocked(boolean value) {#setLocked-boolean}
```
public void setLocked(boolean value)
```


Especifica si este estilo está bloqueado.

 **Examples:** 

Muestra cómo bloquear un estilo.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Establece el nombre del estilo.

 **Remarks:** 

No puede ser una cadena vacía.

Si ya existe un estilo con ese nombre en la colección, este estilo lo sobrescribirá. Todos los nodos afectados harán referencia al nuevo estilo.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del estilo. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado.

 **Remarks:** 

Esta propiedad no es utilizada por Aspose.Words. El siguiente estilo de párrafo solo se aplicará automáticamente cuando edite el documento en MS Word.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setPriority(int value) {#setPriority-int}
```
public void setPriority(int value)
```


Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas Estilos.

 **Examples:** 

Muestra cómo priorizar y ocultar un estilo.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añade a la derecha del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir a la derecha del contenido de las celdas de la tabla. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int}
```
public void setRowStripe(int value)
```


Establece un número de filas que se incluirán en la banda cuando el estilo especifica bandas de filas impares/pares.

 **Examples:** 

Muestra cómo crear estilos de tabla condicionales que alternan entre filas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | Un número de filas a incluir en el sombreado cuando el estilo especifica sombreado de filas impares/pares. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setSemiHidden(boolean value) {#setSemiHidden-boolean}
```
public void setSemiHidden(boolean value)
```


Obtiene/establece si el estilo se oculta de la galería Estilos y del panel de tareas Estilos.

 **Examples:** 

Muestra cómo priorizar y ocultar un estilo.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añade encima del contenido de las celdas de la tabla.

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir encima del contenido de las celdas de la tabla. |

### setUnhideWhenUsed(boolean value) {#setUnhideWhenUsed-boolean}
```
public void setUnhideWhenUsed(boolean value)
```


Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas de Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos.

 **Examples:** 

Muestra cómo priorizar y ocultar un estilo.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Especifica la alineación vertical para las celdas.

 **Remarks:** 

El valor predeterminado es [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/\#TOP).

 **Examples:** 

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes de [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/). |

