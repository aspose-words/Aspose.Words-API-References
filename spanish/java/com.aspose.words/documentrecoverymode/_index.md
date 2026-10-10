---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words para Java"
description: "Especifica las opciones de recuperación disponibles cuando un documento encuentra errores durante la carga en Java."
type: docs
weight: 171
url: /es/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Especifica las opciones de recuperación disponibles cuando un documento encuentra errores durante la carga.

 **Examples:** 

Muestra cómo intentar recuperar un documento si se produjeron errores durante la carga.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [NONE](#NONE) | No se intenta la recuperación. |
| [TRY_RECOVER](#TRY-RECOVER) | Intenta recuperar el documento preservando la mayor cantidad de datos posible. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


No se intenta la recuperación. Si el documento es inválido, la carga fallará con un error.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Intenta recuperar el documento preservando la mayor cantidad de datos posible.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
