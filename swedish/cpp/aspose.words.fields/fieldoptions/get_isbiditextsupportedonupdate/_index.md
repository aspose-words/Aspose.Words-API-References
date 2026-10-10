---
title: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate metod"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate metod. Hämtar eller anger värdet som indikerar om bidirektional text är fullt stöd under fältuppdatering eller inte i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Hämtar eller anger värdet som indikerar om bidi‑text fullt stödjs under fältuppdatering eller inte.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Anmärkningar


När denna egenskap är inställd på **true**, utförs ytterligare steg för att producera ett fältresultat som är kompatibelt med språk som skrivs från höger till vänster (t.ex. arabiska eller hebreiska) under uppdateringen.

När denna egenskap är inställd på **false** och ett språk som skrivs från höger till vänster används, garanteras inte korrektheten i fältresultatet efter uppdateringen.

Standardvärdet är **false**.

## Exempel



Visar hur man använder [FieldOptions](../) för att säkerställa att fältuppdatering fullt stödjer bidirektional text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Säkerställ att alla fältoperationer som involverar text från höger till vänster utförs som förväntat.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Använd en dokumentbyggare för att infoga ett fält som innehåller text från höger till vänster.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## Se även

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
