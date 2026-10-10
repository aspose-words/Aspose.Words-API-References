---
title: "Aspose::Words::PageSetup::get_Bidi yöntemi"
linktitle: "get_Bidi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_Bidi yöntemi. Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini C++'de belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir.

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Açıklamalar


**true** olduğunda, bu bölümdeki sütunlar sağdan sola doğru düzenlenir.

## Örnekler



Bir bölümde metin sütunlarının sırasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Sütunları sayfanın sağ tarafından başlatmak için "Bidi" özelliğini "true" olarak ayarlayın.
// Sütunların sırası, sağdan sola metin yönüyle eşleşecektir.
// Sütunları sayfanın sol tarafından başlatmak için "Bidi" özelliğini "false" olarak ayarlayın.
// Sütunların sırası, soldan sağa metin yönüyle eşleşecektir.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
