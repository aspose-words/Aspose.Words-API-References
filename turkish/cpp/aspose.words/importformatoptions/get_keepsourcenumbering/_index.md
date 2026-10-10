---
title: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering method"
linktitle: "get_KeepSourceNumbering"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering yöntemi. Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da false'dur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


Kaynak ve hedef belgelerde numaralandırma çakıştığında nasıl içe aktarılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## Örnekler



Numaralı listeler içeren bir belgenin nasıl içe aktarılacağını gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak hedef belgeye herhangi bir liste numarası ithal etmeyin.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayarak tüm çakışan
// liste stili numaralandırmasını, kaynak belgede olduğu gibi aynı görünüme sahip şekilde ithal edin.
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


Aynı liste tanım tanımlayıcısına sahip listeler içeren belgeler içe aktarılırken bir çakışmanın nasıl çözüleceğini gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Farklı bir liste tanım kimliği uygulamak için "KeepSourceNumbering" özelliğini "true" olarak ayarlayın
// Aspose.Words'ün bunları hedef belgelere aynı stillerle aktarması gibi.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Kaynak ve hedef belgelerdeki liste numaralandırma çakışmalarının nasıl çözüleceğini gösterir.
```cpp
// Özel bir liste numaralandırma şemasıyla bir belge açın ve ardından onu klonlayın.
// Her ikisi de aynı numaralandırma formatına sahip olduğundan, bir belgeyi diğerine içe aktarırsak formatlar çakışacaktır.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Belgenin klonunu orijinale içe aktarıp ardından eklediğimizde,
// aynı liste formatına sahip iki liste birleştirilecektir.
// "KeepSourceNumbering" bayrağını "false" olarak ayarlarsak, belge klonundan gelen liste
// orijinale eklediğimizde, eklediğimiz listenin numaralandırmasını sürdürecektir.
// Bu, iki listeyi etkili bir şekilde tek bir listeye birleştirecektir.
// "KeepSourceNumbering" bayrağını "true" olarak ayarlarsak, belge klonu
// listesi orijinal numaralandırmasını koruyacak ve iki liste ayrı listeler gibi görünecektir.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
