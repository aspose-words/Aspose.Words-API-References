---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents metod"
linktitle: "InsertTableOfContents"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents metod. Infogar ett TOC (innehållsförteckning) fält i dokumentet i C++."
type: docs
weight: 48000
url: /sv/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Infogar ett TOC (innehållsförteckning) fält i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| växlar | const System::String\& | Växlarna för TOC-fältet. |
## Anmärkningar


Denna metod infogar ett TOC (innehållsförteckning) fält i dokumentet på den aktuella positionen.

En innehållsförteckning i ett Word-dokument kan byggas på flera sätt och formateras med en mängd olika alternativ. Hur tabellen byggs och visas av Microsoft Word styrs av fältväxlarna.

Det enklaste sättet att ange växlarna är att infoga och konfigurera en innehållsförteckning i ett Word-dokument med menyn Insert->Reference->Index och [Tables](../../../aspose.words.tables/) menyn, sedan slå på visning av fältkoder för att se växlarna. Du kan trycka Alt+F9 i Microsoft Word för att växla visning av fältkoder på eller av.

Till exempel, efter att ha skapat en innehållsförteckning, infogas följande fält i dokumentet: **%{ TOC \o "1-3" \h \z }**. Du kan kopiera **%\o "1-3" \h \z** och använda det som växelparameter.

Observera att [InsertTableOfContents()](../) bara infogar ett TOC-fält, men faktiskt inte bygger innehållsförteckningen. Innehållsförteckningen byggs av Microsoft Word när fältet uppdateras.

Om du infogar en innehållsförteckning med den här metoden och sedan öppnar filen i Microsoft Word, kommer du inte att se innehållsförteckningen eftersom TOC-fältet ännu inte har uppdaterats.

I Microsoft Word uppdateras fält inte automatiskt när ett dokument öppnas, men du kan uppdatera fält i ett dokument när som helst genom att trycka på F9.

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

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
