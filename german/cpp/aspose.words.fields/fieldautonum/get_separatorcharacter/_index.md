---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter Methode"
linktitle: "get_SeparatorCharacter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter Methode. Gibt das Trennzeichen zurück oder legt es fest, das in C++ verwendet wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Ermittelt oder legt das zu verwendende Trennzeichen fest.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Beispiele



Zeigt, wie Absätze mit Autonum-Feldern nummeriert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Jedes AUTONUM-Feld zeigt den aktuellen Wert einer laufenden Zählung von AUTONUM-Feldern an,
// was es uns ermöglicht, Elemente automatisch zu nummerieren, wie bei einer nummerierten Liste.
// Dieses Feld zeigt die Zahl "1." an.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Das Trennzeichen, das im Feldergebnis unmittelbar nach der Zahl erscheint, ist standardmäßig ein Punkt.
// Wenn wir diese Eigenschaft null lassen, wird unser zweites AUTONUM-Feld im Dokument "2." anzeigen.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Wir können diese Eigenschaft so einstellen, dass das erste Zeichen seiner Zeichenkette als neues Trennzeichen verwendet wird.
// In diesem Fall wird unser AUTONUM-Feld nun "2:" anzeigen.
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Siehe auch

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
