---
title: "Aspose::Words::Paragraph::GetText yöntemi"
linktitle: "GetText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::GetText yöntemi. Bu paragrafın metnini paragraf sonu karakteri dahil olmak üzere C++'ta alır."
type: docs
weight: 27000
url: /tr/cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


Bu paragrafın metnini, paragraf sonu karakteri dahil olmak üzere alır.

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## Açıklamalar


Tüm alt düğümlerin metni birleştirilir ve paragraf sonu karakteri aşağıdaki gibi eklenir:

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



Dönen dize, [ControlChar](../../controlchar/) içinde açıklandığı gibi tüm kontrol ve özel karakterleri içerir.

## Örnekler



[CompositeNode](../../compositenode/) öğesinin çocuk koleksiyonunda alt düğümlerin nasıl ekleneceğini, güncelleneceğini ve silineceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge, varsayılan olarak bir paragraf içerir.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Paragrafımız gibi birleşik düğümler, diğer birleşik ve satır içi düğümleri çocuk olarak içerebilir.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Üç tane daha run düğümü oluştur.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Belge gövdesi, bu run'ları bir birleşik düğüme ekleyene kadar göstermez
// ki kendisi belge düğüm ağacının bir parçasıdır, ilk run ile yaptığımız gibi.
// Eklediğimiz düğümlerin metin içeriklerinin nerede olduğunu belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirterek belgedeki konumunu belirleyebiliriz.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// İkinci run'ı, ilk run'ın önüne paragrafta ekleyin.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Üçüncü run'ı, ilk run'dan sonra ekleyin.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// İlk run'ı, paragrafın çocuk düğüm koleksiyonunun başına ekleyin.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Mevcut çocuk düğümleri düzenleyerek ve silerek run'ın içeriğini değiştirebiliriz.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
