---
title: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode metodu"
linktitle: "get_RecoveryMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode yöntemi. Yükleme sırasında hatalar oluştuğunda belgenin nasıl ele alınacağını tanımlar. Sistem belgenin kurtarılmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer C++'da TryRecover'dir."
type: docs
weight: 14500
url: /tr/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Yükleme sırasında hatalar oluştuğunda belgenin nasıl ele alınacağını tanımlar. Sistem belgenin kurtarılmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [TryRecover](../../documentrecoverymode/)'dır.

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Örnekler



Yükleme sırasında hatalar oluştuysa bir belgeyi kurtarmaya nasıl çalışılacağını gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Ayrıca Bakınız

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
