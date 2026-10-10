---
title: "metodo Aspose::Words::Loading::LoadOptions::get_RecoveryMode"
linktitle: "get_RecoveryMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode metodo. Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Usa questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è TryRecover in C++."
type: docs
weight: 14500
url: /it/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Usa questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Esempi



Mostra come provare a recuperare un documento se si sono verificati errori durante il caricamento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Vedi anche

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
