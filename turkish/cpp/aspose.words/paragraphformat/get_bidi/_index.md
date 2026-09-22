---
title: "Aspose::Words::ParagraphFormat::get_Bidi method"
linktitle: "get_Bidi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_Bidi yöntemi. Bunun C++'da sağdan sola bir paragraf olup olmadığını alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Bunun sağdan sola bir paragraf olup olmadığını alır veya ayarlar.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Açıklamalar


**true** olduğunda, bu paragraftaki koşullar ve diğer satır içi nesneler sağdan sola yerleştirilir.

## Örnekler



BIDIOUTLINE alanlarıyla sağdan sola dillerle uyumlu listelerin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// BIDIOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragraflara numara verir,
// ancak sadece sağdan sola düzenleme dili etkin olduğunda, örneğin İbranice veya Arapça, görünür.
// Aşağıdaki alan ".1" görüntüleyecek, bu "1." liste numarasının sağdan sola eşdeğeridir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// İki tane daha BIDIOUTLINE alanı ekleyin, bunlar ".2" ve ".3" görüntüleyecek.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Belgedeki her paragraf için yatay metin hizalamasını sağdan sola (RTL) olarak ayarlayın.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Microsoft Word'de sağdan sola bir düzenleme dili etkinleştirirsek, alanlarımız sayıları gösterecek.
// Aksi takdirde "###" görüntüleyecekler.
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Düz metin belgesinin metin yönünün nasıl algılanacağını gösterir.
```cpp
// "TxtLoadOptions" nesnesi oluşturun, bunu bir belgenin yapıcısına geçirebiliriz
// düz metin belgesini nasıl yüklediğimizi değiştirmek için.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// "DocumentDirection" özelliğini "DocumentDirection.Auto" olarak ayarlayın, otomatik olarak algılar
// Aspose.Words'ın düz metinden yüklediği her paragrafın yönünü.
// Her paragrafın "Bidi" özelliği yönünü saklayacaktır.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// İbranice metni sağdan sola olarak algıla.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// İngilizce metni sağdan sola olarak algıla.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
