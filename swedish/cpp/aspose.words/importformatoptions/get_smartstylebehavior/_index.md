---
title: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior metod"
linktitle: "get_SmartStyleBehavior"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior metod. Hämtar eller anger ett booleskt värde som specificerar hur stilar importeras när de har samma namn i käll- och destinationsdokument. Standardvärdet är false i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Hämtar eller anger ett booleskt värde som specificerar hur stilar ska importeras när de har samma namn i käll- och måldokument. Standardvärdet är **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Anmärkningar


När detta alternativ är **aktiverat**, kommer källstilen att expanderas till direkta attribut i ett destinationsdokument, om [KeepSourceFormatting](../../importformatmode/) importläge används.

När detta alternativ är **inaktiverat**, kommer källstilen att expanderas endast om den är numrerad. Befintliga destinationsattribut kommer inte att skrivas över, inklusive listor.

## Exempel



Visar hur man löser dubblettstilar vid infogning av dokument.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Klona dokumentet och redigera klonens "MyStyle"-stil, så att den har en annan färg än originalet.
// Om vi infogar klonen i originaldokumentet, kommer de två stilarna med samma namn att orsaka en konflikt.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// När vi aktiverar SmartStyleBehavior och använder importformatläget KeepSourceFormatting,
// Aspose.Words kommer att lösa stilkonflikter genom att konvertera källdokumentets stilar.
// med samma namn som destinationsstilar till direkta styckeattribut.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
