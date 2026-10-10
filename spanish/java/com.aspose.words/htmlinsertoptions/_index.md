---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words para Java"
description: "Especifica opciones para el método MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions en Java."
type: docs
weight: 381
url: /es/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

Especifica opciones para el método **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**.

 **Examples:** 

Muestra cómo permite preservar mejor los bordes y márgenes observados.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [NONE](#NONE) | Utilice las opciones predeterminadas al insertar HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Conserve las propiedades de los elementos de nivel de bloque. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Elimine el párrafo vacío que normalmente se inserta después de HTML que termina con un elemento de nivel de bloque. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | Utilice la fuente y el formato de párrafo especificados en [DocumentBuilder](../../com.aspose.words/documentbuilder/) como formato base para el texto insertado desde HTML. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
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


Utilice las opciones predeterminadas al insertar HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Conserve las propiedades de los elementos de nivel de bloque.

 **Remarks:** 

Por defecto, las propiedades de los bloques padre se fusionan y se almacenan en sus elementos hijos (p. ej., párrafos o tablas). Si se especifica esta opción, las propiedades de cada bloque se almacenan por separado en una estructura lógica especial. Como resultado, esta opción permite preservar mejor los bordes y márgenes individuales que aparecen en el documento HTML y obtener mejores resultados de conversión. La desventaja es que el documento resultante se vuelve más difícil de modificar, ya que los bordes y márgenes almacenados en la estructura lógica no están disponibles para su edición.

Solo se conservan los márgenes y bordes de los elementos HTML 'body', 'div' y 'blockquote'. Las propiedades de cada elemento HTML se almacenan por separado.

Si se especifica esta opción, Aspose.Words imita el comportamiento de MS Word respecto a la importación de propiedades de bloque.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Elimine el párrafo vacío que normalmente se inserta después de HTML que termina con un elemento de nivel de bloque.

 **Remarks:** 

Por defecto, [DocumentBuilder](../../com.aspose.words/documentbuilder/) se asegura de que el último elemento de nivel de bloque importado desde HTML se cierre después de la importación e inserta un salto de párrafo después del elemento. Este salto de párrafo separa el contenido importado desde HTML del contenido del documento plantilla. Sin embargo, si un fragmento HTML se inserta en un párrafo vacío, ese salto de párrafo creará un párrafo vacío adicional. Si este comportamiento no es deseado, especifique esta opción.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


Utilice la fuente y el formato de párrafo especificados en [DocumentBuilder](../../com.aspose.words/documentbuilder/) como formato base para el texto insertado desde HTML.

 **Remarks:** 

Si no se especifica esta opción, se ignora el formato de [DocumentBuilder](../../com.aspose.words/documentbuilder/) y el texto se inserta con el formato HTML predeterminado. Como resultado, el texto se muestra tal como se renderiza en los navegadores.

Si se especifica esta opción, el formato del texto insertado se basa en el formato especificado en [DocumentBuilder](../../com.aspose.words/documentbuilder/), y el texto se muestra como si se hubiera insertado usando [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
