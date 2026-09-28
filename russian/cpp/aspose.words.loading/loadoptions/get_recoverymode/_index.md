---
title: "метод Aspose::Words::Loading::LoadOptions::get_RecoveryMode"
linktitle: "get_RecoveryMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode метод. Определяет, как документ должен обрабатываться при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должен ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — TryRecover в C++."
type: docs
weight: 14500
url: /ru/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Определяет, как документ должен обрабатываться при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должна ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Примеры



Показывает, как попытаться восстановить документ, если при загрузке возникли ошибки.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## См. также

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
