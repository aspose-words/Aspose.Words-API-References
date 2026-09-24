---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words para Java"
description: "Proporciona información sobre el nombre y la versión actuales del producto en Java."
type: docs
weight: 51
url: /es/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Proporciona información sobre el nombre y la versión del producto actual.

Para obtener más información, visite el artículo de documentación [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents].

 **Examples:** 

Muestra cómo mostrar información sobre la versión instalada de Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Métodos

| Método | Descripción |
| --- | --- |
| [getProduct()](#getProduct) | Obtiene el nombre completo del producto. |
| [getVersion()](#getVersion) | Obtiene la versión del producto. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Obtiene el nombre completo del producto.

 **Examples:** 

Muestra cómo mostrar información sobre la versión instalada de Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - El nombre completo del producto.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Obtiene la versión del producto.

 **Remarks:** 

La versión del producto está en el formato "Major.Minor.Hotfix.0".

 **Examples:** 

Muestra cómo mostrar información sobre la versión instalada de Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - La versión del producto.
