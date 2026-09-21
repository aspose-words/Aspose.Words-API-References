---
title: "Aspose::Words::Fields::FieldAdvance::get_UpOffset‑metod"
linktitle: "get_UpOffset"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAdvance::get_UpOffset‑metod. Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas uppåt i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fields/fieldadvance/get_upoffset/
---
## FieldAdvance::get_UpOffset method


Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas uppåt.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_UpOffset()
```


## Exempel



Visar hur man infogar ett ADVANCE-fält och redigerar dess egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Nedan finns två sätt att använda ADVANCE-fältet för att justera positionen för den text som följer efter det.
// Effekterna av ett ADVANCE-fält fortsätter att tillämpas tills stycket avslutas,
// eller ett annat ADVANCE-fält uppdaterar offset-/koordinatvärdena.
// 1 -  Ange en riktad offset:
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

// 2 -  Flytta text till en position som anges av koordinater:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Se även

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
