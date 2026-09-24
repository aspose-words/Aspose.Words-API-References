---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se fusiona el formato al importar contenido de otro documento en Java."
type: docs
weight: 400
url: /es/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Especifica cómo se fusiona el formato al importar contenido de otro documento.

 **Remarks:** 

Al copiar nodos de un documento a otro, esta opción especifica cómo se resuelve el formato cuando ambos documentos tienen un estilo con el mismo nombre, pero con formato diferente.

El formato se resuelve de la siguiente manera:

1.  Los estilos incorporados se emparejan usando su identificador de estilo independiente de la configuración regional. Los estilos definidos por el usuario se emparejan usando el nombre del estilo sensible a mayúsculas.
2.  Si no se encuentra un estilo coincidente en el documento de destino, el estilo (y todos los estilos referenciados por él) se copian al documento de destino y los nodos importados se actualizan para referenciar el nuevo estilo.
3.  Si ya existe un estilo coincidente en el documento de destino, lo que ocurre depende del parámetro  importFormatMode  que se pasa a **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** como se describe a continuación.

Al usar la opción [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES), si ya existe un estilo coincidente en el documento de destino, el estilo no se copia y los nodos importados se actualizan para referenciar el estilo existente.

La desventaja de usar [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) es que el texto importado puede verse diferente en el documento de destino en comparación con el documento de origen. Por ejemplo, el estilo "Heading 1" en el documento de origen usa la fuente Arial 16 pt y el estilo "Heading 1" en el documento de destino usa la fuente Times New Roman 14 pt. Al importar texto con el estilo "Heading 1" sin otro formato directo, aparecerá con la fuente Times New Roman 14 pt en el documento de destino.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

La desventaja de usar [KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) es que, si realizas varias importaciones, podrías terminar con muchos estilos en el documento de destino y eso podría dificultar el uso de un formato de estilo coherente en Microsoft Word para este documento.

Usar la opción [KEEP\_DIFFERENT\_STYLES](../../com.aspose.words/importformatmode/\#KEEP-DIFFERENT-STYLES) permite reutilizar los estilos del destino si el formato que proporcionan es idéntico a los estilos del documento de origen. Si el estilo en el documento de destino es diferente del origen, entonces se importa.

 **Examples:** 

Muestra cómo insertar un documento en otro documento.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Campos

| Campo | Descripción |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Solo copia los estilos que son diferentes de los del documento de origen. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Copia todos los estilos necesarios al documento de destino, genera nombres de estilo únicos si es necesario. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Utiliza los estilos del documento de destino y copia los estilos nuevos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Solo copia los estilos que son diferentes de los del documento de origen.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Copia todos los estilos necesarios al documento de destino, genera nombres de estilo únicos si es necesario.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Utiliza los estilos del documento de destino y copia los estilos nuevos. Esta es la opción predeterminada.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
