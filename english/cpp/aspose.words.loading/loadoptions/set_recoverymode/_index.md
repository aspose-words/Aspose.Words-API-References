---
title: Aspose::Words::Loading::LoadOptions::set_RecoveryMode method
linktitle: set_RecoveryMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::set_RecoveryMode method. Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is TryRecover in C++.'
type: docs
weight: 31500
url: /cpp/aspose.words.loading/loadoptions/set_recoverymode/
---
## LoadOptions::set_RecoveryMode method


Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is [TryRecover](../../documentrecoverymode/).

```cpp
void Aspose::Words::Loading::LoadOptions::set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode value)
```

## Examples


Shows how to try to recover a document if errors occurred during loading.

```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```
## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
