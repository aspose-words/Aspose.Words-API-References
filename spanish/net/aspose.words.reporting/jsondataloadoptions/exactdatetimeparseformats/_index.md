---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words para .NET
description: JsonDataLoadOptions ExactDateTimeParseFormats propiedad. Obtiene o establece formatos exactos para analizar valores de fecha y hora JSON mientras se carga JSON. El valor predeterminado esnulo  en C#.
type: docs
weight: 30
url: /es/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Obtiene o establece formatos exactos para analizar valores de fecha y hora JSON mientras se carga JSON. El valor predeterminado es`nulo` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Observaciones

Las cadenas codificadas con el formato de fecha y hora JSON de Microsoft® (por ejemplo, "/Fecha(1224043200000)/") siempre se reconocen como valores de fecha y hora independientemente del valor de esta propiedad. La propiedad define formatos adicionales que se utilizarán al analizar valores de fecha y hora de cadenas de la siguiente manera:

* cuando`ExactDateTimeParseFormats` es`nulo` el formato ISO-8601 y todos los formatos de fecha y hora admitidos para las culturas actuales, inglés de EE. UU. e inglés de Nueva Zelanda, se utilizan adicionalmente en el orden mencionado.
* cuando`ExactDateTimeParseFormats` contiene cadenas, se utilizan como formatos adicionales de fecha y hora utilizando la cultura actual.
* cuando`ExactDateTimeParseFormats` está vacío, no se utilizan formatos de fecha y hora adicionales.

### Ver también

* class [JsonDataLoadOptions](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
