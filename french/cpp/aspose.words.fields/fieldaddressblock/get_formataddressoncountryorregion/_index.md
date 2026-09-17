---
title: "Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion méthode"
linktitle: "get_FormatAddressOnCountryOrRegion"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion méthode. Obtient ou définit si l'adresse doit être formatée selon le pays/région du destinataire tel que défini par POST*CODE (Union postale universelle 2006) en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldaddressblock/get_formataddressoncountryorregion/
---
## FieldAddressBlock::get_FormatAddressOnCountryOrRegion method


Obtient ou définit si l'adresse doit être formatée selon le pays/région du destinataire tel que défini par POST*CODE (Union postale universelle 2006).

```cpp
bool Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion()
```


## Exemples



Montre comment insérer un champ ADDRESSBLOCK.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Définir ceci à \"2\" inclura tous les pays et régions,
// à moins que ce ne soit celui spécifié dans la propriété ExcludedCountryOrRegionName.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// Par défaut, cette propriété contiendra l'ID de langue du premier caractère du document.
// Nous pouvons définir une culture différente pour le champ afin de formater le résultat ainsi.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## Voir aussi

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
