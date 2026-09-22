---
title: "Aspose::Words::Math::OfficeMath::get_NodeType metodu"
linktitle: "get_NodeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Math::OfficeMath::get_NodeType metodu. C++'da OfficeMath döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.math/officemath/get_nodetype/
---
## OfficeMath::get_NodeType method


[OfficeMath](../../../aspose.words/nodetype/) döndürür.

```cpp
Aspose::Words::NodeType Aspose::Words::Math::OfficeMath::get_NodeType() const override
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

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
