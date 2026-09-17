---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore méthode"
linktitle: "get_PageBreakBefore"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore méthode. Vrai si un saut de page est imposé avant le paragraphe en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


Vrai si un saut de page est forcé avant le paragraphe.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Exemples



Montre comment créer des paragraphes avec des sauts de page au début.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez ce drapeau sur "vrai" pour appliquer un saut de page au début de chaque paragraphe
// que le constructeur de document créera sous cette configuration ParagraphFormat.
// Le premier paragraphe ne recevra pas de saut de page.
// Laissez ce drapeau sur "faux" pour commencer chaque nouveau paragraphe sur la même page
// comme le précédent, à condition qu'il y ait suffisamment d'espace.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
