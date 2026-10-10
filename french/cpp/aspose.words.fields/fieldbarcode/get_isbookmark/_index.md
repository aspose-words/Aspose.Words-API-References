---
title: "Aspose::Words::Fields::FieldBarcode::get_IsBookmark méthode"
linktitle: "get_IsBookmark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldBarcode::get_IsBookmark méthode. Obtient ou définit si PostalAddress est le nom d'un signet en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldbarcode/get_isbookmark/
---
## FieldBarcode::get_IsBookmark method


Obtient ou définit si [PostalAddress](../get_postaladdress/) est le nom d'un signet.

```cpp
bool Aspose::Words::Fields::FieldBarcode::get_IsBookmark()
```


## Exemples



Montre comment utiliser le champ BARCODE pour afficher les codes ZIP américains sous forme de code-barres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Voici deux façons d'utiliser les champs BARCODE pour afficher des valeurs personnalisées sous forme de codes-barres.
// 1 -  Enregistrez la valeur que le code-barres affichera dans la propriété PostalAddress :
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Cette valeur doit être un code postal valide.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Référencez un signet qui stocke la valeur que ce code-barres affichera :
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// Le signet que le champ BARCODE référence dans sa propriété PostalAddress
// doit contenir uniquement le code postal valide.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Voir aussi

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
