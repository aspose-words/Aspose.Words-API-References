---
title: "Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields Methode"
linktitle: "get_UpdateDirtyFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields Methode. Gibt an, ob die Felder mit dem Dirty-Attribut in C++ aktualisiert werden sollen."
type: docs
weight: 17000
url: /de/cpp/aspose.words.loading/loadoptions/get_updatedirtyfields/
---
## LoadOptions::get_UpdateDirtyFields method


Gibt an, ob Felder mit dem **dirty**‑Attribut aktualisiert werden sollen.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields() const
```


## Beispiele



Zeigt, wie man die spezielle Eigenschaft zum Aktualisieren des Feld-Ergebnisses verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geben Sie den integrierten "Author"-Eigenschaftswert des Dokuments an und zeigen Sie ihn anschließend in einem Feld an.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Aktualisieren Sie die Eigenschaft. Das Feld zeigt immer noch den alten Wert an.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Da der Feldwert veraltet ist, können wir ihn als "dirty" markieren.
// Dieser Wert bleibt veraltet, bis wir das Feld manuell mit der Methode Field.Update() aktualisieren.
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Wenn wir speichern, ohne eine Aktualisierungsmethode aufzurufen,
    // wird das Feld weiterhin den veralteten Wert im Ausgabedokument anzeigen.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // Das LoadOptions-Objekt verfügt über eine Option, alle Felder zu aktualisieren.
    // Als \"dirty\" markiert beim Laden des Dokuments.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Das Aktualisieren von dirty-Feldern auf diese Weise setzt automatisch deren \"IsDirty\"-Flag auf false.
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

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
