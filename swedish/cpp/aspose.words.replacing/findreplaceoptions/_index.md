---
title: "Aspose::Words::Replacing::FindReplaceOptions klass"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions klass. Anger alternativ för sök/ersätt‑operationer. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Anger alternativ för sök/ersätt‑operationer. För att lära dig mer, besök artikeln [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) documentation article.

```cpp
class FindReplaceOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Initierar en ny instans av klassen [FindReplaceOptions](./) med standardinställningar. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Initierar en ny instans av klassen [FindReplaceOptions](./) med den angivna riktningen. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Initierar en ny instans av klassen [FindReplaceOptions](./) med den angivna ersättnings‑callbacken. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Initierar en ny instans av klassen [FindReplaceOptions](./) med den angivna riktningen och ersättnings‑callbacken. |
| [get_ApplyFont](./get_applyfont/)() const | Textformatering som tillämpas på nytt innehåll. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | [Paragraph](../../aspose.words/paragraph/) formatering som tillämpas på nytt innehåll. |
| [get_Direction](./get_direction/)() const | Väljer riktning för ersättning. Standardvärdet är [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True indikerar att oldValue måste vara ett fristående ord. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Hämtar eller anger ett booleskt värde som indikerar om text inuti raderingsrevisioner ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Hämtar eller anger ett booleskt värde som indikerar om text inuti fältkoder ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Hämtar eller anger ett booleskt värde som indikerar om text inuti fält ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Hämtar eller anger ett booleskt värde som indikerar om fotnoter ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Hämtar eller anger ett booleskt värde som indikerar om text inuti infogningsrevisioner ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Hämtar eller anger ett booleskt värde som indikerar om text inuti OfficeMath/> ska ignoreras. Standardvärdet är **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Hämtar eller anger ett booleskt värde som indikerar om former inom en text ska ignoreras. Standardvärdet är **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Hämtar eller anger ett booleskt värde som indikerar om innehållet i [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) ska ignoreras. Standardvärdet är **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Hämtar eller anger ett booleskt värde som indikerar att den gamla sök/ersätt-algoritmen används. |
| [get_MatchCase](./get_matchcase/)() const | True indikerar skiftlägeskänslig jämförelse, false indikerar skiftlägesokänslig jämförelse. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Anger formatet för ersättningen. Standard är [Text](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | Den användardefinierade metoden som anropas före varje ersättningsförekomst. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Hämtar eller anger ett booleskt värde som indikerar om det är tillåtet att ersätta styckeavbrott när det inte finns något nästa syskonstycke. Standardvärdet är **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True indikerar att en textsökning utförs sekventiellt från toppen till botten med hänsyn till textrutor. Standardvärdet är **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Hämtar eller anger ett booleskt värde som indikerar om substitutioner inom ersättningsmönster ska kännas igen och användas. Standardvärdet är **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Väljer riktning för ersättning. Standardvärdet är [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Anger formatet för ersättningen. Standard är [Text](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Den användardefinierade metoden som anropas före varje ersättningsförekomst. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True indikerar att en textsökning utförs sekventiellt från toppen till botten med hänsyn till textrutor. Standardvärdet är **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Sättare för [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man växlar skiftlägeskänslighet vid en sök‑och‑ersätt‑operation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "MatchCase" till "true" för att tillämpa skiftlägeskänslighet när du söker efter strängar att ersätta.
// Ställ in flaggan "MatchCase" till "false" för att ignorera teckenkänslighet när du söker efter text att ersätta.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Visar hur man växlar fristående ord‑endast sök‑och‑ersätt‑operationer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "FindWholeWordsOnly" till "true" för att ersätta den hittade texten om den inte är en del av ett annat ord.
// Ställ in flaggan "FindWholeWordsOnly" till "false" för att ersätta all text oavsett dess omgivning.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Se även

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
