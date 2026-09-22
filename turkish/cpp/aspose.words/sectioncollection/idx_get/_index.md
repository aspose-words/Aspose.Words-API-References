---
title: "Aspose::Words::SectionCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SectionCollection::idx_get yöntemi. C++'ta verilen indeksteki bir bölümü alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


Verilen indeksdeki bölümü getirir.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Bölümler listesindeki bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

## Örnekler



Belge sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bir belgeyi PDF'ye, bir görüntüye kaydetmek ya da ilk kez yazdırmak otomatik olarak
// belgenin sayfaları içinde düzeni önbelleğe alır.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Mevcut Aspose.Words sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzeni istersek
// güncel kalması için, manuel olarak güncellememiz gerekecek.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```


Yeni bir bölüm düğümünü düzenleme için nasıl hazırlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölümle gelir, bu bölümün bir body'si vardır ve bu body'nin bir paragraph'ı vardır.
// Bu belgeye içerik eklemek için o paragrafın içine text runs, shapes veya tables gibi öğeler ekleyebiliriz.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Böyle bir yeni bölüm eklersek, bir body'si veya başka herhangi bir alt düğümü olmayacaktır.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// "EnsureMinimum" yöntemini çalıştırarak bu bölüme bir body ve bir paragraf ekleyin, böylece düzenlemeye başlayabilirsiniz.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
