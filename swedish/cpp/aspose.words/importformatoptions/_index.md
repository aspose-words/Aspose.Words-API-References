---
title: "Aspose::Words::ImportFormatOptions klass"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions klass. Gör det möjligt att ange olika importalternativ för att formatera utdata. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Tillåter att specificera olika importalternativ för att formatera utdata. För att lära dig mer, besök dokumentationsartikeln [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) i dokumentationen.

```cpp
class ImportFormatOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Hämtar eller anger ett booleskt värde som specificerar om menings- och ordavstånd ska justeras automatiskt. Standardvärdet är **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | Hämtar eller anger ett booleskt värde som indikerar om den första importerade avsnittstypen ska ändras till [NewPage](../sectionstart/) tvångsmässigt när [AppendDocument()](../) anropas. Standardvärdet är **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Hämtar eller anger ett booleskt värde som indikerar om motstridiga stilar ska kopieras i läget [KeepSourceFormatting](../importformatmode/). Standardvärdet är **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | Hämtar eller anger ett booleskt värde som specificerar att källformatering av rubrik-/fotsektioners innehåll ignoreras om läget [KeepSourceFormatting](../importformatmode/) används. Standardvärdet är **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | Hämtar eller anger ett booleskt värde som specificerar att källformatering av textrutors innehåll ignoreras om läget [KeepSourceFormatting](../importformatmode/) används. Standardvärdet är **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Hämtar eller anger ett booleskt värde som specificerar hur numrering ska importeras när den krockar i käll- och måldokument. Standardvärdet är **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Hämtar eller anger ett booleskt värde som specificerar om inklistrade listor ska slås ihop med omgivande listor. Standardvärdet är **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Hämtar eller anger ett booleskt värde som specificerar om temafärger för former ska lösas tvångsmässigt. Standardvärdet är **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Hämtar eller anger ett booleskt värde som specificerar hur stilar ska importeras när de har samma namn i käll- och måldokument. Standardvärdet är **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Sättare för [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
