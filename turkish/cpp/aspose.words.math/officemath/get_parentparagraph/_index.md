---
title: "Aspose::Words::Math::OfficeMath::get_ParentParagraph metodu"
linktitle: "get_ParentParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Math::OfficeMath::get_ParentParagraph metodu. C++'da bu düğümün üst Paragraph'ını alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.math/officemath/get_parentparagraph/
---
## OfficeMath::get_ParentParagraph method


Bu düğümün üst [Paragraph](../../../aspose.words/paragraph/) öğesini alır.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Math::OfficeMath::get_ParentParagraph()
```


## Örnekler



Office math görüntüleme biçimlendirmesinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Diğer OfficeMath düğümlerinin çocuğu olan OfficeMath düğümleri her zaman satır içi olur.
// Üzerinde çalıştığımız düğüm, konum ve görüntüleme türünü değiştirmek için temel düğümdür.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// OfficeMath düğümünün konum ve görüntüleme türünü değiştir.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Ayrıca Bakınız

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
