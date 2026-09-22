---
title: "Aspose::Words::IHyphenationCallback::RequestDictionary yöntemi. Belirtilen dil için heceleme sözlüğünün bulunamadığını ve kaydedilmesi gerekebileceğini uygulamaya bildirir. Uygulama bir sözlük bulmalı ve RegisterDictionary() yöntemlerini kullanarak kaydetmelidir. Eğer sözlük belirtilen dil için mevcut değilse, uygulama aynı dil için daha fazla çağrıyı RegisterDictionary() null değeriyle C++'da devre dışı bırakabilir."
linktitle: "Aspose::Words::IHyphenationCallback::GetType yöntemi"
second_title: "C++ için Aspose.Words API Referansı"
description: "C++'da Aspose::Words::IHyphenationCallback sınıfının GetType metodunu nasıl kullanılır?"
type: docs
weight: 4000
url: /tr/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Uygulamayı, belirtilen dil için heceleme sözlüğünün bulunmadığını ve kaydedilmesi gerekebileceğini bildirir. Uygulama, bir sözlük bulmalı ve [RegisterDictionary()](../) yöntemlerini kullanarak kaydetmelidir. Eğer sözlük belirtilen dil için mevcut değilse, uygulama aynı dil için sonraki çağrılardan **null** değeriyle [RegisterDictionary()](../) kullanarak vazgeçebilir.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dil | System::String | Bir dil adı, ör. "en-US". "culture name" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |

## Ayrıca Bakınız

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
