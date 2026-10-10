---
title: "Aspose::Words::MailMerging::IMailMergeDataSource gränssnitt"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::IMailMergeDataSource gränssnitt. Implementera detta gränssnitt för att möjliggöra kopplad utskrift från en anpassad datakälla, såsom en lista med objekt. Master‑detail‑data stöds också i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implementera detta gränssnitt för att möjliggöra mail merge från en anpassad datakälla, till exempel en lista med objekt. Master‑detail‑data stöds också.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Returnerar namnet på datakällan. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Aspose.Words‑motor för kopplad utskrift anropar den här metoden när den stöter på början av ett nästlat kopplat utskriftsområde. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Går vidare till nästa post i datakällan. |
| static [Type](./type/)() |  |
## Anmärkningar


När en datakälla skapas bör den initieras så att den pekar på BOF (innan den första posten). Aspose.Words‑motor för kopplad utskrift kommer att anropa [MoveNext](./movenext/) för att gå till nästa post och sedan anropa [GetValue()](./getvalue/) för varje sammanslagningsfält den stöter på i dokumentet eller det aktuella kopplade utskriftsområdet.

## Se även

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
