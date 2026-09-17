---
title: "Aspose::Words::Fields::FieldInclude::get_BookmarkName méthode"
linktitle: "get_BookmarkName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldInclude::get_BookmarkName méthode. Obtient ou définit le nom du signet dans le document à inclure en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldinclude/get_bookmarkname/
---
## FieldInclude::get_BookmarkName method


Obtient ou définit le nom du signet dans le document à inclure.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_BookmarkName() override
```


## Exemples



Montre comment créer un champ INCLUDE et définir ses propriétés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nous pouvons utiliser un champ INCLUDE pour importer une partie d'un autre document dans le système de fichiers local.
// Le signet du autre document que nous référencions avec ce champ contient cette partie importée.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Voir aussi

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
