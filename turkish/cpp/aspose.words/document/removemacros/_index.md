---
title: "Aspose::Words::Document::RemoveMacros yöntemi"
linktitle: "RemoveMacros"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::RemoveMacros yöntemi. Belgeden tüm makroları (VBA projesi) ve ayrıca araç çubuklarını ve komut özelleştirmelerini C++'ta kaldırır."
type: docs
weight: 69000
url: /tr/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Belgeden tüm makroları (VBA projesi) ve ayrıca araç çubukları ile komut özelleştirmelerini kaldırır.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Açıklamalar


Bir belgeden tüm makroları kaldırarak belgenin makro virüsleri içermediğinden emin olabilirsiniz.

## Örnekler



Bir belgeden tüm makroların nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Belgenin VBA projesini ve tüm makrolarını kaldırın.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
