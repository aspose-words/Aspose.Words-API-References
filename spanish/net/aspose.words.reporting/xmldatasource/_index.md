---
title: Class XmlDataSource
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Reporting.XmlDataSource clase. Proporciona acceso a los datos de un archivo o secuencia XML para utilizarlos en un informe.
type: docs
weight: 4750
url: /es/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Proporciona acceso a los datos de un archivo o secuencia XML para utilizarlos en un informe.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) artículo de documentación.

```csharp
public class XmlDataSource
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(Stream) | Crea una nueva fuente de datos con datos de una secuencia XML usando opciones predeterminadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(string) | Crea una nueva fuente de datos con datos de un archivo XML utilizando las opciones predeterminadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(Stream, Stream) | Crea una nueva fuente de datos con datos de una secuencia XML utilizando una secuencia de definición de esquema XML. Las opciones predeterminadas se utilizan para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(Stream, XmlDataLoadOptions) | Crea una nueva fuente de datos con datos de una secuencia XML utilizando las opciones especificadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(string, string) | Crea una nueva fuente de datos con datos de un archivo XML utilizando un archivo de definición de esquema XML. Las opciones predeterminadas se utilizan para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(string, XmlDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo XML utilizando las opciones especificadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(Stream, Stream, XmlDataLoadOptions) | Crea una nueva fuente de datos con datos de una secuencia XML utilizando una secuencia de definición de esquema XML. Las opciones especificadas se utilizan para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(string, string, XmlDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo XML utilizando un archivo de definición de esquema XML. Las opciones especificadas se utilizan para la carga de datos XML. |

### Observaciones

Para acceder a los datos del archivo o flujo correspondiente mientras genera un informe, pase una instancia de esta clase como una fuente de datos a uno de[`ReportingEngine`](../reportingengine/) .BuildReport sobrecargas.

En documentos de plantilla, si un elemento XML de nivel superior contiene solo una lista de elementos del mismo tipo, un`XmlDataSource` La instancia debe tratarse de la misma manera que si fuera unDataTable instancia. De lo contrario, un`XmlDataSource` La instancia debe tratarse de la misma manera que si fuera unDataRow instancia. Para obtener más información, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Cuando se pasa la definición de esquema XML a un constructor de esta clase, los tipos de datos de valores de elementos XML simples y los atributos se determinan según el esquema. Entonces, en los documentos de plantilla, puede trabajar con valores escritos en lugar de solo cadenas.

Cuando la definición de esquema XML no se pasa a un constructor de esta clase, los tipos de datos de valores de elementos XML simples y los atributos se determinan automáticamente según sus representaciones de cadena. Entonces, en documentos de plantilla, en este caso también puedes trabajar con valores escritos. El motor es capaz de reconocer automáticamente valores de los siguientes tipos:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Tenga en cuenta que para que funcione el reconocimiento automático de tipos de datos, las representaciones de cadenas de valores de elementos XML simples y atributos deben formarse utilizando configuraciones culturales invariantes.

Para anular el comportamiento predeterminado de la carga de datos XML, inicialice y pase un[`XmlDataLoadOptions`](../xmldataloadoptions/) instancia a un constructor de esta clase.

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)


