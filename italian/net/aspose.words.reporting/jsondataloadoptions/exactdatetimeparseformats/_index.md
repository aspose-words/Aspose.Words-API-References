---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
second_title: Aspose.Words per .NET API Reference
description: JsonDataLoadOptions proprietà. Ottiene o imposta formati esatti per lanalisi dei valori di data e ora JSON durante il caricamento di JSON. Limpostazione predefinita ènullo .
type: docs
weight: 30
url: /it/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Ottiene o imposta formati esatti per l'analisi dei valori di data e ora JSON durante il caricamento di JSON. L'impostazione predefinita è`nullo` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

### Osservazioni

Le stringhe codificate utilizzando il formato data-ora Microsoft® JSON (ad esempio, "/Date(1224043200000)/") sono sempre riconosciute come valori data-ora indipendentemente dal valore di questa proprietà. La proprietà definisce formati aggiuntivi da utilizzare durante l'analisi dei valori di data e ora dalle stringhe nel modo seguente:

* Quando`ExactDateTimeParseFormats` È`nullo` il formato ISO-8601 e tutti i formati data/ora supportati per le impostazioni cultura attuali, inglese USA e inglese neozelandese vengono utilizzati inoltre nell' ordine menzionato.
* Quando`ExactDateTimeParseFormats` contiene stringhe, vengono utilizzate come formati data-ora aggiuntivi utilizzando le impostazioni cultura correnti.
* Quando`ExactDateTimeParseFormats` è vuoto, non vengono utilizzati formati data-ora aggiuntivi.

### Guarda anche

* class [JsonDataLoadOptions](../)
* spazio dei nomi [Aspose.Words.Reporting](../../jsondataloadoptions/)
* assemblea [Aspose.Words](../../../)


