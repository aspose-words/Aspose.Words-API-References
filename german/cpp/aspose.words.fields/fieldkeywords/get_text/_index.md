---
title: "Aspose::Words::Fields::FieldKeywords::get_Text Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldKeywords::get_Text Methode. Gibt den Text der Schlüsselwörter zurück oder setzt ihn in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Liest oder setzt den Text der Schlüsselwörter.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Beispiele



Zeigt, wie ein KEYWORDS-Feld eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige Schlüsselwörter hinzu, die im Datei-Explorer auch als "Tags" bezeichnet werden.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// Das KEYWORDS-Feld zeigt den Wert dieser Eigenschaft an.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Setzen eines Werts für die Text-Eigenschaft des Feldes,
// und das Aktualisieren des Feldes überschreibt dann auch die entsprechende integrierte Eigenschaft mit dem neuen Wert.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## Siehe auch

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
