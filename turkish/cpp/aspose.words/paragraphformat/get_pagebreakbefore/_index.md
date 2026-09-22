---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore yöntemi"
linktitle: "get_PageBreakBefore"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore yöntemi. C++'ta paragrafın önünde bir sayfa sonu zorlanıyorsa true döner."
type: docs
weight: 27000
url: /tr/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


True, paragraftan önce bir sayfa sonu zorlanıyorsa.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Örnekler



Paragrafların başında sayfa sonlarıyla nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu bayrağı "true" olarak ayarlayarak her paragrafın başına bir sayfa sonu uygular
// bu ParagraphFormat yapılandırması altında belge oluşturucu tarafından oluşturulacak.
// İlk paragraf bir sayfa sonu almayacaktır.
// Her yeni paragrafı aynı sayfada başlatmak için bu bayrağı "false" olarak bırakın
// öncekine benzer, yeterli alan olduğu sürece.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
