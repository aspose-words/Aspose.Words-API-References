---
title: "Méthode Aspose::Words::Fields::FieldHyperlink::get_IsImageMap"
linktitle: "get_IsImageMap"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldHyperlink::get_IsImageMap. Obtient ou définit si des coordonnées doivent être ajoutées au lien hypertexte pour une carte d'image côté serveur en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldhyperlink/get_isimagemap/
---
## FieldHyperlink::get_IsImageMap method


Obtient ou définit si des coordonnées doivent être ajoutées au lien hypertexte pour une carte d'image côté serveur.

```cpp
bool Aspose::Words::Fields::FieldHyperlink::get_IsImageMap()
```


## Exemples



Montre comment utiliser les champs HYPERLINK pour lier des documents dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Lorsque nous cliquons sur ce champ HYPERLINK dans Microsoft Word,
// il ouvrira le document lié puis placera le curseur au signet spécifié.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Lorsque nous cliquons sur ce champ HYPERLINK dans Microsoft Word,
// il ouvrira le document lié et fera automatiquement défiler jusqu'à l'iframe spécifié.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Voir aussi

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
