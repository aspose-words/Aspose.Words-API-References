---
title: "Aspose::Words::MailMerging::FieldMergingArgs::get_Text méthode"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::FieldMergingArgs::get_Text méthode. Obtient ou définit le texte qui sera inséré dans le document pour le champ de fusion actuel en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


Obtient ou définit le texte qui sera inséré dans le document pour le champ de fusion actuel.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## Remarques


Lorsque votre gestionnaire d'événements est appelé, cette propriété est définie sur **null**.

Si vous laissez Text à **null**, le moteur de fusion de courrier insérera [FieldValue](../../fieldmergingargsbase/get_fieldvalue/) à la place du champ de fusion.

Si vous définissez Text sur n'importe quelle chaîne (y compris vide), la chaîne sera insérée dans le document à la place du champ de fusion.
## Voir aussi

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
