---
title: Enum JsonSimpleValueParseMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Reporting.JsonSimpleValueParseMode uppräkning. Anger ett läge för att analysera JSON enkla värden null boolean nummer heltal och sträng när JSON laddas. Ett sådant läge påverkar inte analysen av datumtidvärden.
type: docs
weight: 4440
url: /sv/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Anger ett läge för att analysera JSON enkla värden (null, boolean, nummer, heltal och sträng) när JSON laddas. Ett sådant läge påverkar inte analysen av datum-tid-värden.

```csharp
public enum JsonSimpleValueParseMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Loose | `0` | Anger läget där typer av JSON enkla värden bestäms vid analys av deras strängrepresentationer. Till exempel bestäms typen av 'prop' från JSON-kodavsnittet '{ prop: "123" }' som heltal i detta läge. |
| Strict | `1` | Anger läget där typer av enkla JSON-värden bestäms från själva JSON-notationen. Till exempel bestäms typen av 'prop' från JSON-kodavsnittet '{ prop: "123" }' som sträng i detta läge. |

### Se även

* namnutrymme [Aspose.Words.Reporting](../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../)


