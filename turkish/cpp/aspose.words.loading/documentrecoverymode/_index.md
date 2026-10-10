---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. C++'ta bir belge yüklenirken hatalar oluştuğunda kullanılabilir kurtarma seçeneklerini belirtir."
type: docs
weight: 13500
url: /tr/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Bir belge yüklenirken hatalarla karşılaştığında kullanılabilir kurtarma seçeneklerini belirtir.

```cpp
enum class DocumentRecoveryMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Kurtarma denenmez. Belge geçersizse, yükleme bir hata ile başarısız olur. |
| TryRecover | 1 | Belgeyi mümkün olduğunca çok veri koruyarak kurtarmaya çalışır. |


## Örnekler



Yükleme sırasında hatalar oluştuysa bir belgeyi kurtarmaya nasıl çalışılacağını gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
