---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags metodu"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags metodu. StructuredDocumentTag içeriğini yok sayıp saymayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da false."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Bir boolean değer alır veya ayarlar; bu değer [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) içeriğini yok sayıp saymayacağını gösterir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Açıklamalar


Bu seçenek **true** olarak ayarlandığında, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) içeriği basit bir metin olarak kabul edilecektir.

Aksi takdirde, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) bağımsız bir [Story](../../../aspose.words/story/) olarak işlenecek ve değiştirme deseni her bir [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) için ayrı ayrı aranacaktır; böylece desen bir [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) içinde kesişirse, o desen için değiştirme uygulanmayacaktır.

## Örnekler



Etiketlerin içeriğinin değiştirmeden nasıl yok sayılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Bu paragraf SDT içerir.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
