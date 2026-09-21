---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop metod"
linktitle: "get_LinesToDrop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop metod. Hämtar eller anger antalet rader i stycket som används för att beräkna höjden på en drop cap i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Hämtar eller anger antalet rader i styckets text som används för att beräkna höjden på initialbokstaven.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Exempel



Visar hur man ställer in storleken på en drop cap.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ändra egenskapen "LinesToDrop" för att ange ett stycke som en drop cap,
// vilket kommer att göra det till en stor versal som dekorerar nästa stycke.
// Ge denna egenskap värdet 4 för att ge drop cap höjden av fyra textrader.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Återställ egenskapen "LinesToDrop" till 0 för att göra nästa stycke till ett vanligt stycke.
// Texten i detta stycke kommer att flöda runt drop cap.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
