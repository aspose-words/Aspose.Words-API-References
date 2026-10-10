---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. Anger de tillgängliga återställningsalternativen när ett dokument stöter på fel under inläsning i C++."
type: docs
weight: 13500
url: /sv/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Anger de tillgängliga återställningsalternativen när ett dokument stöter på fel under laddning.

```cpp
enum class DocumentRecoveryMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Ingen återställning försöks. Om dokumentet är ogiltigt kommer inläsning att misslyckas med ett fel. |
| TryRecover | 1 | Försöker återställa dokumentet samtidigt som så mycket data som möjligt bevaras. |


## Exempel



Visar hur man försöker återställa ett dokument om fel uppstod under inläsning.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
