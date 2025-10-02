---
title: Aspose::Words::Loading::DocumentRecoveryMode enum
linktitle: DocumentRecoveryMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::DocumentRecoveryMode enum. Specifies the available recovery options when a document encounters errors during loading in C++.'
type: docs
weight: 13500
url: /cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Specifies the available recovery options when a document encounters errors during loading.

```cpp
enum class DocumentRecoveryMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No recovery is attempted. If the document is invalid, loading will fail with an error. |
| TryRecover | 1 | Attempts to recover the document while preserving as much data as possible. |


## Examples



Shows how to try to recover a document if errors occurred during loading. 
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
