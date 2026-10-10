---
title: "Aspose::Words::LowCode::MailMergeOptions class"
linktitle: "MailMergeOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::MailMergeOptions-klass. Representerar alternativ för sammanslagningsfunktionaliteten i C++."
type: docs
weight: 750
url: /sv/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Representerar alternativ för mailmerge-funktionaliteten.

```cpp
class MailMergeOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Hämtar en uppsättning flaggor som specificerar vilka objekt som ska tas bort under sammanslagning. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Hämtar eller anger ett värde som indikerar om stycken med skiljetecken betraktas som tomma och ska tas bort om alternativet [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) är specificerat. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Hämtar ett värde som indikerar om alla dokumentets sammanslagningsregioner med namnet på en datakälla ska slås samman vid körning av en sammanslagning med regioner mot datakällan eller bara den första. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Hämtar ett värde som indikerar om fält i hela dokumentet uppdateras vid körning av en sammanslagning med regioner. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Hämtar ett värde som indikerar om de oanvända \"mustache\"-taggarna ska bevaras. |
| [get_RegionEndTag](./get_regionendtag/)() const | Hämtar en sluttagg för sammanslagningsregion. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Hämtar en starttagg för sammanslagningsregion. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Hämtar ett värde som indikerar om listor startas om i varje avsnitt efter att en sammanslagning har körts. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Hämtar ett värde som indikerar om avsnittets början för det första dokumentavsnittet och dess kopior för efterföljande datakällrader behålls under sammanslagning eller uppdateras enligt MS Words beteende. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Hämtar ett värde som indikerar om efterföljande och inledande blanksteg tas bort från sammanslagningsvärden. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Hämtar ett värde som indikerar om sammanslagningsfält och sammanslagningsregioner slås samman oavsett föräldrafältet IF:s villkor. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | När **true**, specificerar att förutom MERGEFIELD-fält utförs sammanslagning i vissa andra fälttyper och även i \"{{fieldName}}\"-taggar. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Hämtar ett värde som indikerar om hela stycket med **TableStart**- eller **TableEnd**-fält eller ett specifikt intervall mellan **TableStart**- och **TableEnd**-fält ska inkluderas i sammanslagningsregionen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Ställer in en uppsättning flaggor som specificerar vilka objekt som ska tas bort under sammanslagning. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Sättare för [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Ställer in ett värde som indikerar om alla dokumentets sammanslagningsregioner med namnet på en datakälla ska slås samman vid körning av en sammanslagning med regioner mot datakällan eller bara den första. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Ställer in ett värde som indikerar om fält i hela dokumentet uppdateras vid körning av en sammanslagning med regioner. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Ställer in ett värde som indikerar om de oanvända \"mustache\"-taggarna ska bevaras. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Ställer in en sluttagg för sammanslagningsregion. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Ställer in en starttagg för sammanslagningsregion. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Ställer in ett värde som indikerar om listor startas om i varje avsnitt efter att en sammanslagning har körts. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Ställer in ett värde som indikerar om avsnittets början för det första dokumentavsnittet och dess kopior för efterföljande datakällrader behålls under sammanslagning eller uppdateras enligt MS Words beteende. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Ställer in ett värde som indikerar om efterföljande och inledande blanksteg tas bort från sammanslagningsvärden. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Ställer in ett värde som anger om sammanslagningsfält och sammanslagningsregioner slås samman oavsett föräldra‑IF‑fältets villkor. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Inställare för [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Ställer in ett värde som anger om hela stycket med **TableStart**‑ eller **TableEnd**‑fältet eller ett specifikt intervall mellan **TableStart**‑ och **TableEnd**‑fält bör inkluderas i mail‑sammanfogningsregionen. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
