---
title: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode Methode"
linktitle: "get_RecoveryMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode Methode. Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen, oder ein anderes definiertes Verhalten folgen soll. Der Standardwert ist TryRecover in C++."
type: docs
weight: 14500
url: /de/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen, oder ein anderes definiertes Verhalten folgen soll. Der Standardwert ist [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Beispiele



Zeigt, wie versucht werden kann, ein Dokument wiederherzustellen, wenn beim Laden Fehler aufgetreten sind.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Siehe auch

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
