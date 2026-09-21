---
title: "Aspose::Words::Properties::DocumentSecurity enum"
linktitle: "DocumentSecurity"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentSecurity enum. Används som ett värde för Security-egenskapen. Anger säkerhetsnivån för ett dokument som ett numeriskt värde i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Används som ett värde för egenskapen [Security](../builtindocumentproperties/get_security/). Anger säkerhetsnivån för ett dokument som ett numeriskt värde.

```cpp
enum class DocumentSecurity
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Det finns inga säkerhetstillstånd som specificeras av egenskapen. |
| PasswordProtected | 1 | Dokumentet är lösenordsskyddat. (Observera att detta aldrig har setts i ett dokument hittills). |
| ReadOnlyRecommended | 2 | Dokumentet ska öppnas skrivskyddat om möjligt, men inställningen kan åsidosättas. |
| ReadOnlyEnforced | 4 | Dokumentet ska alltid öppnas skrivskyddat. |
| ReadOnlyExceptAnnotations | 8 | Dokumentet ska alltid öppnas skrivskyddat förutom för kommentarer. |


## Exempel



Visar hur man använder dokumentegenskaper för att visa säkerhetsnivån för ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Om vi konfigurerar ett dokument som skrivskyddat kommer det att visa detta status med den inbyggda egenskapen "Security".
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Skrivskydda ett dokument och verifiera sedan dess säkerhetsnivå.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" är en beskrivande egenskap. Vi kan redigera dess värde manuellt.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## Se även

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
