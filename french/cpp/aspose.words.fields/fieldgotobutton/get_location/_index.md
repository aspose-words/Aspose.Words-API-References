---
title: "Aspose::Words::Fields::FieldGoToButton::get_Location méthode"
linktitle: "get_Location"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldGoToButton::get_Location méthode. Obtient ou définit le nom d'un signet, le numéro de page ou tout autre élément vers lequel sauter en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


Obtient ou définit le nom d'un signet, d'un numéro de page ou d'un autre élément vers lequel sauter.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## Exemples



Montre comment insérer un champ GOTOBUTTON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez un champ GOTOBUTTON. Lorsque nous double-cliquons sur ce champ dans Microsoft Word,
// il déplacera le curseur de texte vers le signet dont le nom est référencé par la propriété Location.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Insérez un signet valide que le champ pourra référencer.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Voir aussi

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
