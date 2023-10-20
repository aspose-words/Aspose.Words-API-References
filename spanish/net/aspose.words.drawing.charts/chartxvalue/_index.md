---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartXValue clase. Representa un valor X para una serie de gráficos en C#.
type: docs
weight: 840
url: /es/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Representa un valor X para una serie de gráficos.

```csharp
public class ChartXValue
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Obtiene el valor de fecha y hora almacenado. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Obtiene el valor numérico almacenado. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Obtiene el valor multinivel almacenado. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Obtiene el valor de la cadena almacenada. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Obtiene el valor de tiempo almacenado. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Obtiene el tipo del valor X almacenado en el objeto. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Crea un`ChartXValue` instancia de laDateTime tipo. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Crea un`ChartXValue` instancia de laDouble tipo. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Crea un`ChartXValue` instancia de laMultilevel tipo. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Crea un`ChartXValue` instancia de laString tipo. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Crea un`ChartXValue` instancia de laTime tipo. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor X actual. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Obtiene un código hash para el objeto de valor X actual. |

## Observaciones

Esta clase contiene varios métodos estáticos para crear un valor X de un tipo particular. El [`ValueType`](./valuetype/) La propiedad le permite determinar el tipo de un valor X existente.

Todos los valores X no nulos de una serie de gráficos deben ser iguales[`ChartXValueType`](../chartxvaluetype/) tipo.

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
