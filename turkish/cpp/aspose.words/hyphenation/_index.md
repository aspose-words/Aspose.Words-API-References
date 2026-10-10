---
title: "Aspose::Words::Hyphenation sınıfı"
linktitle: "Heceleme"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Hyphenation sınıfı. Heceleme sözlükleriyle çalışmak için yöntemler sağlar. Bu sözlükler, belirli bir dildeki kelimelerin nerede hecelenebileceğini belirler. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 33000
url: /tr/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Heceleme sözlükleriyle çalışmak için yöntemler sağlar. Bu sözlükler belirli bir dildeki kelimelerin nerede hecelenebileceğini belirler. Daha fazla bilgi edinmek için [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) dokümantasyon makalesini ziyaret edin.

```cpp
class Hyphenation
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [get_Callback](./get_callback/)() | Belgenin sayfa düzeni oluşturulurken sözlükleri talep etmek için kullanılan geri çağırma arayüzünü alır. Bu, birçok dilde belge işlenirken faydalı olabilecek sözlüklerin gecikmeli yüklenmesini sağlar. |
| static [get_WarningCallback](./get_warningcallback/)() | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, heceleme desenleri yüklenirken çağrılır. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Belirtilen dil için kayıtlı sözlük yoksa veya kayıtlı sözlük Null ise **false**, aksi takdirde **true** döndürür. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Belirtilen dil için bir akıştan heceleme sözlüğü kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçimdeyse istisna fırlatır. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Belirtilen dil için bir dosyadan heceleme sözlüğü kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçimdeyse istisna fırlatır. Bu yöntem aynı dil için [Callback](./get_callback/) tekrar tekrar çağrılmasını önlemek amacıyla Null sözlüğü kaydetmek için de kullanılabilir. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Belgenin sayfa düzeni oluşturulurken sözlükleri talep etmek için kullanılan geri çağırma arayüzünü ayarlar. Bu, birçok dilde belge işlenirken faydalı olabilecek sözlüklerin gecikmeli yüklenmesini sağlar. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, heceleme desenleri yüklenirken çağrılır. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Belirtilen dil için bir heceleme sözlüğünün kaydını siler. Bu, Null sözlüğü kaydetmekten farklıdır. Sözlüğün kaydının silinmesi, belirtilen dil için geri çağırmayı etkinleştirir. |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
