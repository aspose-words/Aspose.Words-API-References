---
title: "XmlDataLoadOptions"
linktitle: "XmlDataLoadOptions"
second_title: "Aspose.Words para Java"
description: "Representa opciones para la carga de datos XML en Java."
type: docs
weight: 745
url: /es/java/com.aspose.words/xmldataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataLoadOptions
```

Representa opciones para la carga de datos XML.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Una instancia de esta clase puede pasarse a los constructores de [XmlDataSource](../../com.aspose.words/xmldatasource/).


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [XmlDataLoadOptions()](#XmlDataLoadOptions) | Inicializa una nueva instancia de esta clase con opciones predeterminadas. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject) | Obtiene una bandera que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz XML. |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean) | Establece una bandera que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz XML. |
### XmlDataLoadOptions() {#XmlDataLoadOptions}
```
public XmlDataLoadOptions()
```


Inicializa una nueva instancia de esta clase con opciones predeterminadas.

### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject}
```
public boolean getAlwaysGenerateRootObject()
```


Obtiene una bandera que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz XML. Si un elemento raíz XML no tiene atributos y todos sus elementos hijos tienen los mismos nombres, dicho objeto no se crea de forma predeterminada.

 **Remarks:** 

El valor predeterminado es  false .

**Returns:**
boolean - Una bandera que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz XML.
### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean}
```
public void setAlwaysGenerateRootObject(boolean value)
```


Establece una bandera que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz XML. Si un elemento raíz XML no tiene atributos y todos sus elementos hijos tienen los mismos nombres, dicho objeto no se crea de forma predeterminada.

 **Remarks:** 

El valor predeterminado es  false .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz XML. |

