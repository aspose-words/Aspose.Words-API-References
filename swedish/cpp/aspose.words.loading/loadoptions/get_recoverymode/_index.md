---
title: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode metod"
linktitle: "get_RecoveryMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode metod. Definierar hur dokumentet ska hanteras om fel uppstår under inläsning. Använd den här egenskapen för att ange om systemet ska försöka återställa dokumentet eller följa ett annat definierat beteende. Standardvärdet är TryRecover i C++."
type: docs
weight: 14500
url: /sv/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Definierar hur dokumentet ska hanteras om fel uppstår under inläsning. Använd den här egenskapen för att ange om systemet ska försöka återställa dokumentet eller följa ett annat definierat beteende. Standardvärdet är [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Exempel



Visar hur man försöker återställa ett dokument om fel uppstod under inläsning.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Se även

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
