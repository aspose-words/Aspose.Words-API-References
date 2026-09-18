---
title: "Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition-Methode"
linktitle: "get_HorizontalPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition-Methode. Gibt die Anzahl der Punkte zurück oder legt sie fest, um die der nach dem Feld folgende Text horizontal von der linken Kante der Spalte, des Rahmens oder der Textbox verschoben werden soll, in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldadvance/get_horizontalposition/
---
## FieldAdvance::get_HorizontalPosition method


Liest oder setzt die Anzahl der Punkte, um die der Text, der dem Feld folgt, horizontal von der linken Kante der Spalte, des Rahmens oder der Textbox verschoben werden soll.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition()
```


## Beispiele



Zeigt, wie ein ADVANCE-Feld eingefügt und dessen Eigenschaften bearbeitet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Im Folgenden werden zwei Methoden gezeigt, wie das ADVANCE-Feld verwendet wird, um die Position des nachfolgenden Textes anzupassen.
// Die Auswirkungen eines ADVANCE-Feldes bleiben wirksam, bis der Absatz endet,
// oder ein anderes ADVANCE-Feld die Versatz-/Koordinatenwerte aktualisiert.
// 1 -  Einen richtungsabhängigen Versatz angeben:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Text zu einer durch Koordinaten angegebenen Position verschieben:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Siehe auch

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
