---
title: "Aspose::Words::DocumentBuilder::InsertHyperlink metod"
linktitle: "InsertHyperlink"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertHyperlink metod. Infogar en hyperlänk i dokumentet i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Infogar en hyperlänk i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| displayText | const System::String\& | Texten för länken som ska visas i dokumentet. |
| urlOrBookmark | const System::String\& | Länkmål. Kan vara en URL eller ett namn på ett bokmärke i dokumentet. Denna metod lägger alltid till apostrofer i början och slutet av URL:en. |
| isBookmark | bool | **true** om föregående parameter är ett namn på ett bokmärke i dokumentet; **false** om föregående parameter är en URL. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.
## Anmärkningar


Observera att du måste ange teckensnittformatering för hyperlänkens visningstext explicit med hjälp av egenskapen [Font](../get_font/).

Denna metod anropar internt [InsertField()](../) för att infoga ett MS Word HYPERLINK-fält i dokumentet.

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


Visar hur man använder en dokumentbyggares formateringsstack.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in teckenformatering, skriv sedan texten som kommer före hyperlänken.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Bevara vår aktuella formateringskonfiguration på stacken.
builder->PushFont();

// Ändra byggarens aktuella formatering genom att tillämpa en ny stil.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Återställ teckenformateringen som vi sparade tidigare och ta bort elementet från stacken.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```


Visar hur man infogar en hyperlänk som refererar till ett lokalt bokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Infoga ett HYPERLINK‑fält som länkar till bokmärket. Vi kan skicka fältväxlar
// till metoden "InsertHyperlink" som en del av argumentet som innehåller det refererade bokmärkets namn.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
