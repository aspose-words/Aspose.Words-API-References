---
title: "Aspose::Words::Section::Clone méthode"
linktitle: "Clone"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section::Clone méthode. Crée un duplicata de cette section en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/section/clone/
---
## Section::Clone method


Crée un duplicata de cette section.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## Exemples



Montre comment ajouter et supprimer des sections dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Supprimez la première section du document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Ajoutez une copie de ce qui est maintenant la première section à la fin du document.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Voir aussi

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
