---
title: "Aspose::Words::Lists::List::HasSameTemplate Methode"
linktitle: "HasSameTemplate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::List::HasSameTemplate Methode. Gibt true zurück, wenn die aktuelle Liste und die angegebene Liste aus derselben Vorlage in C++ erstellt wurden."
type: docs
weight: 14000
url: /de/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Gibt true zurück, wenn die aktuelle Liste und die angegebene Liste aus derselben Vorlage erstellt wurden.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Beispiele



Zeigt, wie man Listen mit derselben ListDefId definiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## Siehe auch

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
