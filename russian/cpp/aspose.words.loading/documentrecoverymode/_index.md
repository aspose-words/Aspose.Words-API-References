---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. Указывает доступные варианты восстановления, когда документ сталкивается с ошибками при загрузке в C++."
type: docs
weight: 13500
url: /ru/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Указывает доступные варианты восстановления, когда документ сталкивается с ошибками во время загрузки.

```cpp
enum class DocumentRecoveryMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Восстановление не будет предпринято. Если документ недействителен, загрузка завершится ошибкой. |
| TryRecover | 1 | Пытается восстановить документ, сохраняя как можно больше данных. |


## Примеры



Показывает, как попытаться восстановить документ, если при загрузке возникли ошибки.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
