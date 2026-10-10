---
title: "Aspose::Words::StyleCollection::get_Count metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection::get_Count‑metod. Hämtar antalet stilar i samlingen i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


Hämtar antalet stilar i samlingen.

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
```


## Exempel



Visar hur man lägger till en [Style](../../style/) i ett dokuments stilsamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i denna samling.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena av
// dess egenskap "DefaultParagraphFormat" på stilens egenskap "ParagraphFormat".
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Lägg till en stil och verifiera sedan att den har standardinställningarna.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Se även

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
