---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se importan las propiedades de los elementos de bloque desde documentos basados en HTML en Java."
type: docs
weight: 39
url: /es/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Especifica cómo se importan las propiedades de los elementos de nivel de bloque desde documentos basados en HTML.

 **Examples:** 

Muestra cómo se importan las propiedades de los elementos de bloque desde documentos basados en HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [MERGE](#MERGE) | Las propiedades de los bloques padre se fusionan y se almacenan en los elementos hijos (p. ej. |
| [PRESERVE](#PRESERVE) | Las propiedades de los bloques padre se importan a una estructura lógica especial y se almacenan por separado de los nodos del documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Las propiedades de los bloques padre se fusionan y se almacenan en los elementos hijos (p. ej. párrafos o tablas).

 **Remarks:** 

Las propiedades de los bloques padre se fusionan de la siguiente manera: los márgenes se suman; los bordes de los bloques de nivel superior se descartan y solo se conservan los bordes del nivel más interno. Como resultado, cuando se especifica este modo, se perderá parte del formato de los bloques del documento original.

Por otro lado, dado que todas las propiedades de bloque fusionadas se almacenan en los nodos del documento, todo el formato en el documento resultante estará disponible para su modificación.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Las propiedades de los bloques padre se importan a una estructura lógica especial y se almacenan por separado de los nodos del documento.

 **Remarks:** 

Solo se importan los márgenes y bordes de los elementos HTML 'body', 'div' y 'blockquote'. Las propiedades de cada elemento HTML se almacenan individualmente.

Este modo permite preservar mejor los bordes y márgenes vistos en el documento HTML y obtener mejores resultados de conversión. La desventaja es que el documento resultante se vuelve más difícil de modificar, ya que los bordes y márgenes almacenados en la estructura lógica no están disponibles para su edición.

Este modo imita el comportamiento de MS Word respecto a la importación de propiedades de bloque.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
