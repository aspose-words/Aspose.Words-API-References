---
title: "Aspose::Words::Fields::FieldSubject::get_Text-Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSubject::get_Text-Methode. Liest oder setzt den Text des Subjekts in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Liefert oder setzt den Text des Betreffs.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Beispiele



Zeigt, wie das SUBJECT-Feld verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Setzen Sie einen Wert für die integrierte Eigenschaft "Subject" des Dokuments.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Erstellen Sie ein SUBJECT-Feld, um den Wert dieser integrierten Eigenschaft anzuzeigen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Wenn wir dem Text‑Eigenschaftswert des SUBJECT-Felds einen Wert zuweisen und es aktualisieren, wird das Feld
// den aktuellen Wert der integrierten Eigenschaft "Subject" mit dem Wert seiner Text‑Eigenschaft überschreiben,
// und anschließend den neuen Wert anzeigen.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## Siehe auch

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
