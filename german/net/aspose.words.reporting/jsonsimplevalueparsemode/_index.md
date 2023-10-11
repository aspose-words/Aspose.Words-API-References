---
title: Enum JsonSimpleValueParseMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Reporting.JsonSimpleValueParseMode opsomming. Gibt einen Modus zum Parsen einfacher JSONWerte Null Boolescher Wert Zahl Ganzzahl und Zeichenfolge beim Laden von JSON an. Ein solcher Modus hat keinen Einfluss auf das Parsen von Datums/Uhrzeitwerten.
type: docs
weight: 4700
url: /de/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Gibt einen Modus zum Parsen einfacher JSON-Werte (Null, Boolescher Wert, Zahl, Ganzzahl und Zeichenfolge) beim Laden von JSON an. Ein solcher Modus hat keinen Einfluss auf das Parsen von Datums-/Uhrzeitwerten.

```csharp
public enum JsonSimpleValueParseMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Loose | `0` | Gibt den Modus an, in dem Typen einfacher JSON-Werte beim Parsen ihrer Zeichenfolgendarstellungen bestimmt werden. Beispielsweise wird der Typ von „prop“ aus dem JSON-Snippet „{ prop: „123“ }“ in diesem Modus als Ganzzahl bestimmt. |
| Strict | `1` | Gibt den Modus an, in dem Typen einfacher JSON-Werte aus der JSON-Notation selbst bestimmt werden. Beispielsweise wird der Typ von „prop“ aus dem JSON-Snippet „{ prop: „123“ }“ in diesem Modus als Zeichenfolge bestimmt. |

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)


