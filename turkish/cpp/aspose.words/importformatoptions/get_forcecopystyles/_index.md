---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles yöntemi"
linktitle: "get_ForceCopyStyles"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles yöntemi. KeepSourceFormatting modunda çakışan stilleri kopyalayıp kopyalamayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta false'dur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


[KeepSourceFormatting](../../importformatmode/) modunda çakışan stilleri kopyalayıp kopyalamayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Açıklamalar


Varsayılan olarak, hedef belgede eşleşen bir stil zaten varsa, kaynak stil biçimlendirmesi doğrudan düğüm özniteliklerine genişletilir ve bu düğümün stili varsayılana sıfırlanır.

Bu seçenek **true** olarak ayarlandığında, kaynak stil benzersiz bir adla hedef belgeye zorla kopyalanır ve içe aktarılan düğüme uygulanır.

Not: bu durumda, hedef belgede içe aktarılan düğümün biçimlendirmesinin korunacağı garanti edilmez.

## Örnekler



Kaynak stillerin benzersiz adlarla zorla nasıl kopyalanacağını gösterir.
```cpp
// Her iki belge de MyStyle1 ve MyStyle2 içerir, MyStyle3 yalnızca kaynak belgede bulunur.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
