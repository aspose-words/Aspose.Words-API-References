---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words för .NET
description: JsonDataLoadOptions ExactDateTimeParseFormats fast egendom. Hämtar eller ställer in exakta format för att analysera JSONdatumtidvärden när JSON laddas. Standard ärnull  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Hämtar eller ställer in exakta format för att analysera JSON-datum-tid-värden när JSON laddas. Standard är`null` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Anmärkningar

Strängar som är kodade med Microsoft® JSON datum-tid-format (till exempel "/Date(1224043200000)/") känns alltid igen som datum-tid-värden oavsett ett värde för den här egenskapen. Egenskapen definierar ytterligare -format som ska användas vid analys av datum-tid-värden från strängar på följande sätt:

* När`ExactDateTimeParseFormats` är`null` ISO-8601-formatet och alla datum-tid-format som stöds för den nuvarande, engelska USA och engelska Nya Zeelands kulturer används dessutom i nämnda ordning.
* När`ExactDateTimeParseFormats` innehåller strängar, de används som ytterligare datum-tid -format med den nuvarande kulturen.
* När`ExactDateTimeParseFormats` är tom, inga ytterligare datum-tid-format används.

### Se även

* class [JsonDataLoadOptions](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
