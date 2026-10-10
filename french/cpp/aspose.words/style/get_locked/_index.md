---
title: "Méthode Aspose::Words::Style::get_Locked"
linktitle: "get_Locked"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Style::get_Locked. Indique si ce style est verrouillé en C++."
type: docs
weight: 13500
url: /fr/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Spécifie si ce style est verrouillé.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Exemples



Montre comment verrouiller le style.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
