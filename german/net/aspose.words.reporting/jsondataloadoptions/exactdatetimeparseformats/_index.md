---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
second_title: Aspose.Words für .NET-API-Referenz
description: JsonDataLoadOptions eigendom. Ruft genaue Formate zum Parsen von JSONDatums/Uhrzeitwerten beim Laden von JSON ab oder legt diese fest. Die Standardeinstellung istNull .
type: docs
weight: 30
url: /de/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Ruft genaue Formate zum Parsen von JSON-Datums-/Uhrzeitwerten beim Laden von JSON ab oder legt diese fest. Die Standardeinstellung ist`Null` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

### Bemerkungen

Zeichenfolgen, die im Microsoft® JSON-Datums-/Uhrzeitformat codiert sind (z. B. „/Date(1224043200000)/“), werden immer als Datums-/Uhrzeitwerte erkannt, unabhängig vom Wert dieser Eigenschaft. Die Eigenschaft definiert zusätzliche -Formate, die beim Parsen von Datums-/Uhrzeitwerten aus Zeichenfolgen auf folgende Weise verwendet werden:

* Wann`ExactDateTimeParseFormats` Ist`Null` das ISO-8601-Format und alle Datums-/Uhrzeitformate, die für die aktuellen, englischen USA- und englischen Neuseeland-Kulturen unterstützt werden, werden zusätzlich in der genannten Reihenfolge verwendet.
* Wann`ExactDateTimeParseFormats` Enthält Zeichenfolgen. Sie werden als zusätzliche Datums-/Uhrzeitformate unter Verwendung der aktuellen Kultur verwendet.
* Wann`ExactDateTimeParseFormats` ist leer, es werden keine zusätzlichen Datums-/Uhrzeitformate verwendet.

### Siehe auch

* class [JsonDataLoadOptions](../)
* namensraum [Aspose.Words.Reporting](../../jsondataloadoptions/)
* Montage [Aspose.Words](../../../)


