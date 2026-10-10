---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words para Java"
description: "Una interfaz de una fábrica para construir implementaciones de ITextShaper en Java."
type: docs
weight: 787
url: /es/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

Una interfaz de una fábrica para construir implementaciones de [ITextShaper](../../com.aspose.words/itextshaper/).
## Métodos

| Método | Descripción |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | Devuelve una nueva instancia de un text shaper para la fuente representada por  fontBlob  y  faceIndex . |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | Devuelve una nueva instancia de un text shaper para la fuente especificada por  fontPath  y  faceIndex . |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Devuelve una nueva instancia de un text shaper para la fuente representada por  fontBlob  y  faceIndex .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontId | java.lang.String | Un identificador único que puede asociarse de forma única con la fuente proporcionada fontBlob. |
| fontBlob | byte[] | Matriz de bytes con los datos de la fuente. |
| faceIndex | int | Un índice de la cara tipográfica en la colección de fuentes TrueType, o 0 si  fontBlob  no es una colección de fuentes TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Devuelve una nueva instancia de un text shaper para la fuente especificada por  fontPath  y  faceIndex .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontPath | java.lang.String | Una ruta absoluta al archivo de fuente. |
| faceIndex | int | Un índice de la cara tipográfica en la colección de fuentes TrueType, o 0 si el archivo de fuente especificado no es una colección de fuentes TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
