---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Math::OfficeMathDisplayType enum. C++'da denklemin görüntü formatı türünü belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Denklemin görüntüleme formatı tipini belirtir.

```cpp
enum class OfficeMathDisplayType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Display | 0 | Office [Math](../) kendi satırında görüntülenir. |
| Inline | 1 | Office [Math](../) metin içinde satır içi görüntülenir. |


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

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
