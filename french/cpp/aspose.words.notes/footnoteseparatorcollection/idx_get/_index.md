---
title: "Méthode Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get. Récupère un FootnoteSeparator du type spécifié en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.notes/footnoteseparatorcollection/idx_get/
---
## FootnoteSeparatorCollection::idx_get method


Récupère un [FootnoteSeparator](../../footnoteseparator/) du type spécifié.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get(Aspose::Words::Notes::FootnoteSeparatorType separatorType)
```


## Exemples



Montre comment gérer le format du séparateur de note de bas de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Aligne le séparateur de note de bas de page.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Voir aussi

* Class [FootnoteSeparator](../../footnoteseparator/)
* Enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* Class [FootnoteSeparatorCollection](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
