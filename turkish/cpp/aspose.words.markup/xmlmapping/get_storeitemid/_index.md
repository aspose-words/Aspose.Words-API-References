---
title: "Aspose::Words::Markup::XmlMapping::get_StoreItemId metodu"
linktitle: "get_StoreItemId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::XmlMapping::get_StoreItemId metodu. C++'ta XPath ifadesini değerlendirmek için kullanılacak özel XML veri bölümünün özel XML veri tanımlayıcısını belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Özel XML veri bölümünün [XPath](../get_xpath/) ifadesini değerlendirmek için kullanılacak özel XML veri tanımlayıcısını belirtir.

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Örnekler



Bir XML bölümünün özel XML veri tanımlayıcısının nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Yapılandırılmış belge etiketlerinin GUID biçiminde kimlikleri vardır.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## Ayrıca Bakınız

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
