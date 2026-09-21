---
title: "Aspose::Words::DocumentBuilder::get_Underline method"
linktitle: "get_Underline"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::get_Underline method. Hämtar/sätter understryknings typ för det aktuella teckensnittet i C++."
type: docs
weight: 26000
url: /sv/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Hämtar/anger understryknings typ för det aktuella teckensnittet.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Exempel



Visar hur man formaterar text som infogats av en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// Byggaren tillämpar formatering på sitt aktuella stycke och all ny text som läggs till av den därefter.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## Se även

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
