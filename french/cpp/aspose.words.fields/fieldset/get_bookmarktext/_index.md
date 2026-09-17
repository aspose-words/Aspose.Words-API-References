---
title: "Méthode Aspose::Words::Fields::FieldSet::get_BookmarkText"
linktitle: "get_BookmarkText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldSet::get_BookmarkText. Obtient ou définit le nouveau texte du signet en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldset/get_bookmarktext/
---
## FieldSet::get_BookmarkText method


Obtient ou définit le nouveau texte du signet.

```cpp
System::String Aspose::Words::Fields::FieldSet::get_BookmarkText()
```


## Exemples



Montre comment créer du texte signet avec un champ SET, puis l'afficher dans le document à l'aide d'un champ REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nommez le texte signet avec un champ SET.
// Ce champ fait référence au "bookmark" pas à une structure de signet qui apparaît dans le texte, mais à une variable nommée.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Faites référence au signet par son nom dans un champ REF et affichez son contenu.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Voir aussi

* Class [FieldSet](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
