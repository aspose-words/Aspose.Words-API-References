---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel méthode"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel méthode. Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'une table des figures qui n'inclut pas le libellé et le numéro de la légende dans C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'une table des figures qui n'inclut pas l'étiquette et le numéro de la légende.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Exemples



Montre comment définir le nom de l'identifiant de séquence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## Voir aussi

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
