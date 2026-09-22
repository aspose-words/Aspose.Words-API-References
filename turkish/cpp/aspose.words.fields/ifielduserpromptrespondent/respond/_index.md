---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond yöntemi"
linktitle: "Respond"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond yöntemi. Uygulandığında, kullanıcıdan gelen yanıtı döndürür. Uygulamanız, kullanıcının isteme yanıt vermediğini göstermek için null döndürmelidir (yani kullanıcı istem penceresinde İptal düğmesine basmıştır) C++'ta."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


Uygulandığında, istem üzerine kullanıcıdan bir yanıt döndürür. Uygulamanız, kullanıcının isteğe yanıt vermediğini göstermek için **null** döndürmelidir (yani kullanıcı istem penceresinde İptal düğmesine basmıştır).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| promptText | System::String | İstem metni (yani istem penceresinin başlığı). |
| defaultResponse | System::String | Varsayılan kullanıcı yanıtı (yani istem penceresinde bulunan başlangıç değeri). |

### ReturnValue

Kullanıcı yanıtı (yani istem penceresinde onaylanan değer).

## Ayrıca Bakınız

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
