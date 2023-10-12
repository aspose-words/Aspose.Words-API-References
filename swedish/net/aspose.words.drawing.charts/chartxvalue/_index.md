---
title: Class ChartXValue
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartXValue klass. Representerar ett Xvärde för en diagramserie.
type: docs
weight: 840
url: /sv/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Representerar ett X-värde för en diagramserie.

```csharp
public class ChartXValue
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Hämtar det lagrade datetime-värdet. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Hämtar det lagrade numeriska värdet. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Hämtar det lagrade flernivåvärdet. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Hämtar det lagrade strängvärdet. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Hämtar det lagrade tidsvärdet. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Hämtar typen av X-värde som lagras i objektet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(DateTime) | Skapar en`ChartXValue` instans avDateTime typ. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(double) | Skapar en`ChartXValue` instans avDouble typ. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(ChartMultilevelValue) | Skapar en`ChartXValue` instans avMultilevel typ. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(string) | Skapar en`ChartXValue` instans avString typ. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(TimeSpan) | Skapar en`ChartXValue` instans avTime typ. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(object) | Får en flagga som indikerar om det angivna objektet är lika med det aktuella X-värdeobjektet. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Hämtar en hashkod för det aktuella X-värdeobjektet. |

### Anmärkningar

Den här klassen innehåller ett antal statiska metoder för att skapa ett X-värde av en viss typ. The [`ValueType`](./valuetype/) egenskap låter dig bestämma typen av ett befintligt X-värde.

Alla X-värden som inte är noll i en diagramserie måste vara av samma[`ChartXValueType`](../chartxvaluetype/) typ.

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


