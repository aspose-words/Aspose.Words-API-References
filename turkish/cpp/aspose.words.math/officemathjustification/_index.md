---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Math::OfficeMathJustification enum. C++'de denklemin hizalamasını belirtir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Denklemin hizalamasını belirtir.

```cpp
enum class OfficeMathJustification
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| CenterGroup | 1 | Matematik metni örneklerini birbirine göre sola hizalar ve matematik metni grubunu ([Math](../)[Paragraph](../../aspose.words/paragraph/)) sayfaya göre ortalar. |
| Orta | 2 | Matematik metni her örneğini kenarlara göre ayrı ayrı ortalar. |
| Left | 3 | [Math](../)[Paragraph](../../aspose.words/paragraph/) sol hizalama. |
| Right | 4 | [Math](../)[Paragraph](../../aspose.words/paragraph/) sağ hizalama. |
| Inline | 7 | [Math](../) için [Inline](../../aspose.words/inline/) konumu. |
| Default | n/a | Varsayılan değer [CenterGroup](./). |


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
