---
title: "Metodo Aspose::Words::Fields::FieldAdvance::get_LeftOffset"
linktitle: "get_LeftOffset"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldAdvance::get_LeftOffset. Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a sinistra in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fields/fieldadvance/get_leftoffset/
---
## FieldAdvance::get_LeftOffset method


Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a sinistra.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_LeftOffset()
```


## Esempi



Mostra come inserire un campo ADVANCE e modificare le sue proprietà.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Di seguito sono riportati due modi per utilizzare il campo ADVANCE per regolare la posizione del testo che lo segue.
// Gli effetti di un campo ADVANCE continuano ad essere applicati fino alla fine del paragrafo,
// o un altro campo ADVANCE aggiorna i valori di offset/coordinate.
// 1 -  Specificare un offset direzionale:
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

// 2 -  Spostare il testo in una posizione specificata dalle coordinate:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Vedi anche

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
