---
title: "Aspose::Words::Fields::Field::get_DisplayResult method"
linktitle: "get_DisplayResult"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field::get_DisplayResult‑metod. Hämtar texten som representerar det visade fältresultatet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Hämtar texten som representerar det visade fältresultatet.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Exempel



Visar hur man får den faktiska texten som ett fält visar i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// Vi kan använda egenskapen DisplayResult för att verifiera exakt vilken text
// ett fält skulle visa på sin plats i dokumentet.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Fält behåller inte korrekta resultatvärden i realtid.
// För att säkerställa att våra fält visar korrekta resultat när som helst,
// till exempel precis före en sparoperation, måste vi uppdatera dem manuellt.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
