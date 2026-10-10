---
title: "Aspose::Words::Underline enum"
linktitle: "Understrykning"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Underline enum. Anger typen av understrykning som tillämpas på ett teckensnitt i C++."
type: docs
weight: 126000
url: /sv/cpp/aspose.words/underline/
---
## Underline enum


Anger typen av understrykning som tillämpas på ett teckensnitt.

```cpp
enum class Underline
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 |  |
| Enkel | 1 |  |
| Ord | 2 |  |
| Dubbel | 3 |  |
| Prickad | 4 |  |
| Tjock | 6 |  |
| Streck | 7 |  |
| Långstreck | 39 |  |
| Punktstreck | 9 |  |
| Punktpunktstreck | 10 |  |
| Vågig | 11 |  |
| Tungprickad | 20 |  |
| Tungstreck | 23 |  |
| Tunglångstreck | 55 |  |
| Tungpunktstreck | 25 |  |
| Tungpunktpunktstreck | 26 |  |
| Tungvågig | 27 |  |
| Dubbelvågig | 43 |  |


## Exempel



Visar hur man infogar ett hyperlänksfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Infoga en hyperlänk och betona den med anpassad formatering.
// Hyperlänken kommer att vara en klickbar textbit som tar oss till den plats som anges i URL:en.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + vänsterklick på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
