---
title: "Méthode Aspose::Words::Paragraph::get_IsFormatRevision"
linktitle: "get_IsFormatRevision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Paragraph::get_IsFormatRevision. Retourne true si le formatage de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Renvoie vrai si le format de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Exemples



Montre comment vérifier si un paragraphe est une révision de format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Ce paragraphe est une révision "Format", qui se produit lorsque nous modifions le formatage du texte existant
// tout en suivant les révisions dans Microsoft Word via \"Review\" -> \"Track changes\".
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## Voir aussi

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
