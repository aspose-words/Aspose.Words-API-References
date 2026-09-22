---
title: "Aspose::Words::IHyphenationCallback interface"
linktitle: "IHyphenationCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IHyphenationCallback arayüzü. C++'ta heceleme sözlüklerini kaydedebilen sınıflar tarafından uygulanır."
type: docs
weight: 78000
url: /tr/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Hecelemesi sözlüklerini kaydedebilen sınıflar tarafından uygulanır.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Uygulamayı, belirtilen dil için heceleme sözlüğünün bulunmadığını ve kaydedilmesi gerekebileceğini bildirir. Uygulama, bir sözlük bulmalı ve [RegisterDictionary()](../) yöntemlerini kullanarak kaydetmelidir. Eğer sözlük belirtilen dil için mevcut değilse, uygulama aynı dil için sonraki çağrılardan **null** değeriyle [RegisterDictionary()](../) kullanarak vazgeçebilir. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
