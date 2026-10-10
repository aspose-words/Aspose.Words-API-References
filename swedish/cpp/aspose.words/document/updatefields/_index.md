---
title: "Aspose::Words::Document::UpdateFields metod"
linktitle: "UpdateFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UpdateFields metod. Uppdaterar värdena för fält i hela dokumentet i C++."
type: docs
weight: 96000
url: /sv/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Uppdaterar värdena för fält i hela dokumentet.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Anmärkningar


När du öppnar, ändrar och sedan sparar ett dokument uppdaterar inte Aspose.Words fält automatiskt, utan behåller dem intakta. Därför vill du vanligtvis anropa den här metoden innan du sparar om du har ändrat dokumentet programmässigt och vill försäkra dig om att de korrekta (beräknade) fältvärdena visas i det sparade dokumentet.

Det finns inget behov av att uppdatera fält efter att ha utfört en kopplad utskick eftersom kopplad utskick är en form av fältuppdatering och automatiskt uppdaterar alla fält i dokumentet.

Denna metod uppdaterar inte alla fälttyper. För en detaljerad lista över stödjade fälttyper, se Programmerarguiden.

Denna metod uppdaterar inte fält som är relaterade till sidlayoutalgoritmer (t.ex. PAGE, PAGES, PAGEREF). Sidlayoutrelaterade fält uppdateras när du renderar ett dokument eller anropar [UpdatePageLayout](../updatepagelayout/).

Använd metoden [NormalizeFieldTypes](../normalizefieldtypes/) innan fältuppdatering om det har skett dokumentändringar som påverkade fälttyper.

För att uppdatera fält i en specifik del av dokumentet, använd [UpdateFields](../../range/updatefields/).

## Exempel



Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med rubrikstilar som poster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen så att den plockar upp stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster så att de blir hyperlänkar som tar oss
// till rubrikens plats när de vänsterklickas i Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Fyll i innehållsförteckningen genom att lägga till stycken med rubrikstilar.
// Varje sådan rubrik med en nivå mellan 1 och 3 kommer att skapa en post i tabellen.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// En innehållsförteckning är ett fält av en typ som måste uppdateras för att visa ett aktuellt resultat.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Visar hur man använder QUOTE-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett QUOTE-fält, som kommer att visa värdet av dess Text-egenskap.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Infoga ett QUOTE-fält och nästla ett DATE-fält inuti det.
// DATE-fält uppdaterar sitt värde till aktuellt datum varje gång vi öppnar dokumentet med Microsoft Word.
// Att nästla DATE-fältet inuti QUOTE-fältet på detta sätt kommer att frysa dess värde
// till datumet då vi skapade dokumentet.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Uppdatera alla fält så att de visar sina korrekta resultat.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Visar hur man ställer in användardetaljer och visar dem med fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett UserInformation-objekt och ange det som datakälla för fält som visar användarinformation.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Infoga fälten USERNAME, USERINITIALS och USERADDRESS, som visar värden av
// de respektive egenskaperna i UserInformation-objektet som vi skapade ovan.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Fältalternativobjektet har också en statisk standardanvändare som fält från alla dokument kan referera till.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
