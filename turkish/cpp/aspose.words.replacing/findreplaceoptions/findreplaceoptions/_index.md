---
title: "Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions yapıcı"
linktitle: "FindReplaceOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions yapıcı. C++'da varsayılan ayarlarla FindReplaceOptions sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


[FindReplaceOptions](../) sınıfının yeni bir örneğini varsayılan ayarlarla başlatır.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## Örnekler



Değiştirme kalıpları içinde yer tutucuları tanıma ve kullanma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Eski modun kullanılması birçok gelişmiş özelliği desteklemez, bu yüzden onu 'false' olarak ayarlamamız gerekir.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


[FindReplaceOptions](../) sınıfının yeni bir örneğini belirtilen yön ile başlatır.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yön | Aspose::Words::Replacing::FindReplaceDirection | Bul ve değiştir işleminin yönü. |

## Ayrıca Bakınız

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


[FindReplaceOptions](../) sınıfının yeni bir örneğini belirtilen yön ve değiştirme geri çağrısı ile başlatır.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yön | Aspose::Words::Replacing::FindReplaceDirection | Bul ve değiştir işleminin yönü. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | Bulunan metni değiştirmek için kullanılacak geri çağrı. |

## Ayrıca Bakınız

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


[FindReplaceOptions](../) sınıfının yeni bir örneğini belirtilen değiştirme geri çağrısı ile başlatır.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | Bulunan metni değiştirmek için kullanılacak geri çağrı. |

## Ayrıca Bakınız

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
