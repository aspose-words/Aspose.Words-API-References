---
title: "Aspose::Words::MailMerging::MailMerge class"
linktitle: "MailMerge"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::MailMerge class. Representerar kopplingsfunktionaliteten. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Representerar mail‑merge‑funktionaliteten. För att lära dig mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [DeleteFields](./deletefields/)() | Tar bort kopplingsrelaterade fält från dokumentet. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Utför en koppling från en anpassad datakälla. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Utför en kopplingsoperation för en enskild post. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Utför en koppling från en anpassad datakälla med kopplingsregioner. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Utför en koppling från en anpassad datakälla med kopplingsregioner. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Hämtar en uppsättning flaggor som specificerar vilka objekt som ska tas bort under sammanslagning. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Hämtar eller anger ett värde som indikerar om stycken med skiljetecken anses vara tomma och ska tas bort om alternativet [RemoveEmptyParagraphs](../mailmergecleanupoptions/) är specificerat. |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Uppstår under koppling när ett kopplingsfält påträffas i dokumentet. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Tillåter att hantera specifika händelser under mail merge. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Returnerar en samling som representerar mappade datafält för mail merge‑operationen. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Hämtar ett värde som indikerar om alla dokumentets sammanslagningsregioner med namnet på en datakälla ska slås samman vid körning av en sammanslagning med regioner mot datakällan eller bara den första. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Hämtar ett värde som indikerar om fält i hela dokumentet uppdateras vid körning av en sammanslagning med regioner. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Hämtar ett värde som indikerar om de oanvända \"mustache\"-taggarna ska bevaras. |
| [get_RegionEndTag](./get_regionendtag/)() const | Hämtar en sluttagg för sammanslagningsregion. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Hämtar en starttagg för sammanslagningsregion. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Hämtar ett värde som indikerar om listor startas om i varje avsnitt efter att en sammanslagning har körts. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Hämtar ett värde som indikerar om [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) för det första dokumentavsnittet och dess kopior för efterföljande datakällrader behålls under mail merge eller uppdateras enligt MS Words beteende. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Hämtar ett värde som indikerar om efterföljande och inledande blanksteg tas bort från sammanslagningsvärden. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Hämtar ett värde som indikerar om sammanslagningsfält och sammanslagningsregioner slås samman oavsett föräldrafältet IF:s villkor. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | När **true**, specificerar att förutom MERGEFIELD-fält utförs sammanslagning i vissa andra fälttyper och även i \"{{fieldName}}\"-taggar. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Hämtar ett värde som indikerar om hela stycket med **TableStart**- eller **TableEnd**-fält eller ett specifikt intervall mellan **TableStart**- och **TableEnd**-fält ska inkluderas i sammanslagningsregionen. |
| [GetFieldNames](./getfieldnames/)() | Returnerar en samling av mail merge‑fältnamn som finns i dokumentet. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Returnerar en samling av mail merge‑fältnamn som finns i regionen. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Returnerar en samling av mail merge‑fältnamn som finns i regionen. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Returnerar en samling av mail merge‑regioner med det angivna namnet. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Returnerar en fullständig hierarki av regioner (med fält) som finns i dokumentet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Ställer in en uppsättning flaggor som specificerar vilka objekt som ska tas bort under sammanslagning. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Sättare för [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Uppstår under koppling när ett kopplingsfält påträffas i dokumentet. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Tillåter att hantera specifika händelser under mail merge. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Ställer in ett värde som indikerar om alla dokumentets sammanslagningsregioner med namnet på en datakälla ska slås samman vid körning av en sammanslagning med regioner mot datakällan eller bara den första. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Ställer in ett värde som indikerar om fält i hela dokumentet uppdateras vid körning av en sammanslagning med regioner. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Ställer in ett värde som indikerar om de oanvända \"mustache\"-taggarna ska bevaras. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Ställer in en sluttagg för sammanslagningsregion. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Ställer in en starttagg för sammanslagningsregion. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Ställer in ett värde som indikerar om listor startas om i varje avsnitt efter att en sammanslagning har körts. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Ställer in ett värde som indikerar om [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) för det första dokumentavsnittet och dess kopior för efterföljande datakällrader behålls under mail merge eller uppdateras enligt MS Words beteende. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Ställer in ett värde som indikerar om efterföljande och inledande blanksteg tas bort från sammanslagningsvärden. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Ställer in ett värde som anger om sammanslagningsfält och sammanslagningsregioner slås samman oavsett föräldra‑IF‑fältets villkor. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Sättare för [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Ställer in ett värde som anger om hela stycket med **TableStart**‑ eller **TableEnd**‑fältet eller ett specifikt intervall mellan **TableStart**‑ och **TableEnd**‑fält bör inkluderas i mail‑sammanfogningsregionen. |
| static [Type](./type/)() |  |
## Anmärkningar


För att mail merge‑operationen ska fungera bör dokumentet innehålla Word MERGEFIELD‑ och eventuellt NEXT‑fält. Under mail merge‑operationen ersätts sammanslagningsfält i dokumentet med värden från din datakälla.

Det finns två olika sätt att använda mail merge: med mail merge‑regioner och utan.

Den enklaste mail merge är utan regioner och den liknar mycket hur mail merge fungerar i Word. Använd **Execute**‑metoder för att slå samman information från någon datakälla såsom **DataTable**, **DataSet** eller en array av objekt till ditt dokument. Objektet [MailMerge](./) bearbetar alla poster i datakällan och kopierar samt lägger till innehållet i hela dokumentet för varje post.

Observera att när objektet [MailMerge](./) stöter på ett NEXT‑fält, väljer det nästa post i datakällan och fortsätter sammanslagningen utan att kopiera något innehåll.

Använd [ExecuteWithRegions()](../) och andra överlagringar för att slå samman information i ett dokument med definierade mail merge‑regioner. Du kan använda dem som datakällor för denna operation.

Du måste använda mail merge‑regioner om du vill dynamiskt utöka delar i dokumentet. Utan mail merge‑regioner kommer hela dokumentet att upprepas för varje post i datakällan.

## Se även

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
