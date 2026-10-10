---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. Specifica le opzioni di recupero disponibili quando un documento incontra errori durante il caricamento in C++."
type: docs
weight: 13500
url: /it/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Specifica le opzioni di recupero disponibili quando un documento incontra errori durante il caricamento.

```cpp
enum class DocumentRecoveryMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Non viene tentato alcun recupero. Se il documento è non valido, il caricamento fallirà con un errore. |
| TryRecover | 1 | Tenta di recuperare il documento preservando il più possibile i dati. |


## Esempi



Mostra come provare a recuperare un documento se si sono verificati errori durante il caricamento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
