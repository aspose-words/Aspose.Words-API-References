---
title: "Méthode Aspose::Words::DocumentBase::get_FootnoteSeparators"
linktitle: "get_FootnoteSeparators"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBase::get_FootnoteSeparators. Fournit l'accès aux séparateurs de notes de bas de page / notes de fin définis dans le document en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Fournit l'accès aux séparateurs de notes de bas de page/notes de fin définis dans le document.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## Exemples



Montre comment supprimer le séparateur de note de fin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Supprimer le séparateur de note de fin.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Montre comment gérer le format du séparateur de note de bas de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Aligne le séparateur de note de bas de page.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Voir aussi

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
