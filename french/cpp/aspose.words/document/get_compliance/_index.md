---
title: "Méthode Aspose::Words::Document::get_Compliance"
linktitle: "get_Compliance"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::get_Compliance. Obtient la version de conformité OOXML déterminée à partir du contenu du document chargé. N'a de sens que pour les documents OOXML en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Obtient la version de conformité OOXML déterminée à partir du contenu du document chargé. N’a de sens que pour les documents OOXML.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Remarques


Si vous avez créé un nouveau document vierge ou chargé un document non OOXML, cela renvoie la valeur [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Exemples



Montre comment lire la version de conformité Open Office XML d'un document chargé.
```cpp
// La version de conformité varie selon les documents créés par différentes versions de Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## Voir aussi

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
