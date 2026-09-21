---
title: "Aspose::Words::Document::Clone metod"
linktitle: "Klona"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::Clone metod. Utför en djup kopiering av Document i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/document/clone/
---
## Document::Clone method


Utför en djup kopiering av [Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

Det klonade dokumentet.

## Exempel



Visar hur man djupt klonar ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Kloning kommer att skapa ett nytt dokument med samma innehåll som originalet,
// men med en unik kopia av varje nod i originaldokumentet.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## Se även

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
