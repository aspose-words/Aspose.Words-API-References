---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::DocumentRecoveryMode‑Enum. Gibt die verfügbaren Wiederherstellungsoptionen an, wenn ein Dokument beim Laden in C++ Fehler auftritt."
type: docs
weight: 13500
url: /de/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Gibt die verfügbaren Wiederherstellungsoptionen an, wenn ein Dokument beim Laden auf Fehler stößt.

```cpp
enum class DocumentRecoveryMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Es wird keine Wiederherstellung versucht. Wenn das Dokument ungültig ist, schlägt das Laden mit einem Fehler fehl. |
| TryRecover | 1 | Versucht, das Dokument wiederherzustellen, wobei möglichst viele Daten erhalten bleiben. |


## Beispiele



Zeigt, wie versucht werden kann, ein Dokument wiederherzustellen, wenn beim Laden Fehler aufgetreten sind.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
