---
title: "Aspose::Words::Fields::Field::get_IsDirty‑metod"
linktitle: "get_IsDirty"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field::get_IsDirty‑metod. Hämtar eller anger om det aktuella resultatet för fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet.

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## Exempel



Visar hur man använder en speciell egenskap för att uppdatera fältresultatet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ge dokumentets inbyggda egenskap \"Author\" ett värde och visa det sedan med ett fält.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Uppdatera egenskapen. Fältet visar fortfarande det gamla värdet.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Eftersom fältets värde är föråldrat kan vi markera det som \"dirty\".
// Detta värde kommer att förbli föråldrat tills vi uppdaterar fältet manuellt med metoden Field.Update().
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Om vi sparar utan att anropa en uppdateringsmetod,
    // kommer fältet fortsätta visa det föråldrade värdet i utmatningsdokumentet.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // LoadOptions‑objektet har ett alternativ för att uppdatera alla fält
    // markerade som \"dirty\" när dokumentet laddas.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Att uppdatera smutsiga fält på detta sätt sätter automatiskt deras \"IsDirty\"‑flagga till falskt.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## Se även

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
