---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words för .NET
description: Optimera anrop av anpassade typer av medlemmar med ReportingEngines egenskap UseReflectionOptimization. Förbättra prestandan med dynamisk klassgenerering för bättre effektivitet.
type: docs
weight: 60
url: /sv/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Hämtar eller ställer in ett värde som anger om anrop av anpassade typmedlemmar som utförs via reflektions-API är optimerade med dynamisk klassgenerering eller inte. Standardvärdet är`sann` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Anmärkningar

Det finns vissa scenarier där det är att föredra att inaktivera denna optimering. Om du till exempel arbetar med små samlingar av dataobjekt hela tiden, kan en overhead för dynamisk klassgenerering vara mer märkbar än en overhead för direkta reflektions-API-anrop. Alternativet har ingen effekt när det körs på iOS och reflektionsoptimering inte används.

### Se även

* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
