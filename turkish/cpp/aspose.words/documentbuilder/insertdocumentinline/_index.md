---
title: "Aspose::Words::DocumentBuilder::InsertDocumentInline yöntemi"
linktitle: "InsertDocumentInline"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertDocumentInline yöntemi. C++'ta imleç konumunda belgeyi satır içi ekler."
type: docs
weight: 33500
url: /tr/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


İmleç konumunda belgeyi satır içi ekler.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Ekleme için kaynak belge. |
| importFormatMode | Aspose::Words::ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Sonuç belgesinin biçimlendirmesini etkileyen seçenekleri belirtmeye olanak tanır. |

### ReturnValue

Eklenen içeriğin ilk düğümü.
## Açıklamalar


Bu yöntem, MS Word davranışını taklit eder; sanki CTRL+'A' (tüm içeriği seç) tuşuna basılmış, ardından CTRL+'C' (seçiliyi tampon belleğe kopyala) bir belgede ve sonra CTRL+'V' (tampon bellekteki içeriği ekle) başka bir belgede yapılmış gibi.

[InsertDocument()](../) yönteminden farklı olarak bu yöntem, hedef belgenin paragrafının içeriğini, kaynak belgenin eklendiği paragraftan önce, eklenen kaynak belgenin son paragrafına taşır. Aslında bu, son eklenen paragrafın paragraf sonu işaretinin kaldırıldığı anlamına gelir.

Not: kaynak belgenin son düğümü bir paragraf değilse, hiçbir işlem yapılmaz.

## Örnekler



İmleç konumunda belgeyi satır içi nasıl ekleyeceğinizi gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Hedef belgeyi oluştur.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Kaynak belgeyi hedefe satır içi ekle.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
