---
title: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator yöntemi"
linktitle: "get_BreakIsStyleSeparator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator yöntemi. Bu paragraf sonu bir Stil Ayırıcı ise true döner. Stil ayırıcı, bir paragrafın farklı paragraf stillerine sahip bölümlerden oluşmasına izin verir C++ içinde."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


Bu paragraf sonu bir [Style](../../style/) Ayırıcı ise true döner. Stil ayırıcı, bir paragrafın farklı paragraf stillerine sahip bölümlerden oluşmasına izin verir.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Örnekler



TOC başlığıyla aynı satıra metin yazmayı ve bunun TOC'ta görünmemesini nasıl yapacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// TOC'nun bir giriş olarak algılayacağı bir stil ile bir paragraf ekleyin.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Bu iki dize aynı paragrafta olduğundan aynı TOC girişinde görünecekler.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Bir stil ayırıcı eklersek, aynı paragrafta daha fazla metin yazabiliriz
// ve farklı bir stil kullanarak TOC'ta görünmelerini engelleyebiliriz.
// Ayırıcıdan sonra bir başlık tipi stil kullanırsak, bir belge metni satırından birden fazla TOC girişi oluşturabiliriz.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
