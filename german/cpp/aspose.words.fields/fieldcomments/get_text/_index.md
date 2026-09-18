---
title: "Aspose::Words::Fields::FieldComments::get_Text Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldComments::get_Text Methode. Liest oder setzt den Text der Kommentare in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Liest oder setzt den Text der Kommentare.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Beispiele



Zeigt, wie das COMMENTS-Feld verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzen Sie einen Wert für die integrierte Eigenschaft "Comments" des Dokuments.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Erstellen Sie ein COMMENTS-Feld, um den Wert dieser integrierten Eigenschaft anzuzeigen.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// Wenn wir der Text‑Eigenschaft des COMMENTS-Feldes einen Wert zuweisen und es aktualisieren, wird das Feld
// den aktuellen Wert der integrierten Eigenschaft "Comments" mit dem Wert seiner Text‑Eigenschaft überschreiben,
// und anschließend den neuen Wert anzeigen.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## Siehe auch

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
