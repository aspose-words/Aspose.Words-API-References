---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words för .NET
description: ReportingEngine UseReflectionOptimization fast egendom. Hämtar eller ställer in ett värde som indikerar om anrop av anpassade typmedlemmar som utförs via reflektionsAPI är optimerade med dynamisk klassgenerering eller inte. Standardvärdet ärSann  i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Hämtar eller ställer in ett värde som indikerar om anrop av anpassade typmedlemmar som utförs via reflektions-API är optimerade med dynamisk klassgenerering eller inte. Standardvärdet är`Sann` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Anmärkningar

Det finns vissa scenarier där det är att föredra att inaktivera denna optimering. Om du till exempel har att göra med små samlingar av dataobjekt hela tiden, kan en overhead av dynamisk klassgenerering vara mer märkbar än en overhead av direktreflektions-API-anrop. Alternativet har ingen effekt när det körs på iOS och reflektionsoptimering används inte.

### Se även

* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
