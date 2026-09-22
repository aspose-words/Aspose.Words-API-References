---
title: "Aspose::Words::NodeImporter::NodeImporter yapıcı"
linktitle: "NodeImporter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeImporter::NodeImporter yapıcı. NodeImporter sınıfının yeni bir örneğini C++'ta başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Yeni bir [NodeImporter](../) sınıf örneği başlatır.

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Kaynak belge. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | İçe aktarılan düğümlerin sahibi olacak hedef belge. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

## Ayrıca Bakınız

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Yeni bir [NodeImporter](../) sınıf örneği başlatır.

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Kaynak belge. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | İçe aktarılan düğümlerin sahibi olacak hedef belge. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | İçe aktarılan düğümü biçimlendirmek için çeşitli seçenekleri belirtir. |

## Örnekler



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

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
