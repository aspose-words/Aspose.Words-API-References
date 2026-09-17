---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. Spécifie le type du séparateur de note de bas de page/de note de fin en C++."
type: docs
weight: 6500
url: /fr/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Spécifie le type du séparateur de note de bas de page/note de fin.

```cpp
enum class FootnoteSeparatorType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| FootnoteSeparator | 0 | Séparateur entre le texte principal et le texte de la note de bas de page. |
| FootnoteContinuationSeparator | 1 | Imprimé au-dessus du texte de la note de bas de page sur une page lorsque le texte doit être poursuivi depuis une page précédente. |
| FootnoteContinuationNotice | 2 | Imprimé sous le texte de la note de bas de page sur une page lorsque le texte de la note de bas de page doit être poursuivi sur une page suivante. |
| EndnoteSeparator | 3 | Séparateur entre le texte principal et le texte de la note de fin. |
| EndnoteContinuationSeparator | 4 | Imprimé au-dessus du texte de la note de fin sur une page lorsque le texte doit être poursuivi depuis une page précédente. |
| EndnoteContinuationNotice | 5 | Imprimé sous le texte de la note de fin sur une page lorsque le texte de la note de fin doit être poursuivi sur une page suivante. |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
