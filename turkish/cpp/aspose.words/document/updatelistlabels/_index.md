---
title: "Aspose::Words::Document::UpdateListLabels yöntemi"
linktitle: "UpdateListLabels"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UpdateListLabels yöntemi. Belgedeki tüm liste öğeleri için liste etiketlerini C++'ta günceller."
type: docs
weight: 97000
url: /tr/cpp/aspose.words/document/updatelistlabels/
---
## Document::UpdateListLabels method


Belgedeki tüm liste öğelerinin liste etiketlerini günceller.

```cpp
void Aspose::Words::Document::UpdateListLabels()
```

## Açıklamalar


Bu yöntem, belgede bulunan her bir [ListLabel](../../paragraph/get_listlabel/) nesnesi için [LabelValue](../../../aspose.words.lists/listlabel/get_labelvalue/) ve [LabelString](../../../aspose.words.lists/listlabel/get_labelstring/) gibi liste etiketi özelliklerini günceller.

Ayrıca, bu yöntem belge alanları güncellenirken bazen dolaylı olarak çağrılır. Bu, TOC veya REF gibi liste numaralarına başvurabilecek bazı alanların güncel olmasını sağlamak için gereklidir.

## Örnekler



Liste öğesi olan tüm paragrafların liste etiketlerini nasıl çıkaracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Paragraf listesinin olup olmadığını bulun. Belgemizde, listemiz sade Arap rakamları kullanıyor,
// ki üçten başlayıp altıya kadar devam eder.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Bu, bu düğümü metin biçiminde çıktıya aldığımızda elde ettiğimiz metindir.
    // Bu metin çıktısı liste etiketlerini atlayacaktır. Herhangi bir paragraf biçimlendirme karakterini temizleyin.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Bu, paragrafın listedeki mevcut seviyedeki konumunu alır. Birden fazla seviyeye sahip bir listemiz varsa,
    // bu, o seviyedeki konumunu bize söyleyecektir.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Çıktıda metinle birlikte liste etiketini eklemek için bunları birleştirin.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
