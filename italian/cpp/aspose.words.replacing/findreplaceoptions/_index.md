---
title: "classe Aspose::Words::Replacing::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Replacing::FindReplaceOptions. Specifica le opzioni per le operazioni di ricerca/sostituzione. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Specifica le opzioni per le operazioni di ricerca/sostituzione. Per saperne di più, visita l'articolo di documentazione [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class FindReplaceOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Inizializza una nuova istanza della classe [FindReplaceOptions](./) con le impostazioni predefinite. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Inizializza una nuova istanza della classe [FindReplaceOptions](./) con la direzione specificata. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Inizializza una nuova istanza della classe [FindReplaceOptions](./) con la callback di sostituzione specificata. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Inizializza una nuova istanza della classe [FindReplaceOptions](./) con la direzione e la callback di sostituzione specificate. |
| [get_ApplyFont](./get_applyfont/)() const | Formattazione del testo applicata al nuovo contenuto. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | Formattazione del [Paragraph](../../aspose.words/paragraph/) applicata al nuovo contenuto. |
| [get_Direction](./get_direction/)() const | Seleziona la direzione per la sostituzione. Il valore predefinito è [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True indica che oldValue deve essere una parola autonoma. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione. Il valore predefinito è **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno dei codici di campo. Il valore predefinito è **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno dei campi. Il valore predefinito è **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Ottiene o imposta un valore booleano che indica se ignorare le note a piè di pagina. Il valore predefinito è **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. Il valore predefinito è **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo. Il valore predefinito è **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Ottiene o imposta un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). Il valore predefinito è **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Ottiene o imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione. |
| [get_MatchCase](./get_matchcase/)() const | True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto non sensibile al maiuscolo/minuscolo. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Specifica il formato della sostituzione. Il valore predefinito è [Testo](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo. Il valore predefinito è **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True indica che la ricerca del testo viene eseguita sequenzialmente dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Ottiene o imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. Il valore predefinito è **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Seleziona la direzione per la sostituzione. Il valore predefinito è [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Specifica il formato della sostituzione. Il valore predefinito è [Testo](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True indica che la ricerca del testo viene eseguita sequenzialmente dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Impostatore per [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come attivare/disattivare la sensibilità al maiuscolo/minuscolo durante un'operazione di ricerca e sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "MatchCase" su "true" per applicare la sensibilità al maiuscolo/minuscolo durante la ricerca delle stringhe da sostituire.
// Imposta il flag "MatchCase" su "false" per ignorare le differenze di maiuscole/minuscole durante la ricerca del testo da sostituire.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Mostra come attivare/disattivare le operazioni di ricerca e sostituzione limitate a parole isolate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo indipendentemente dal contesto.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Vedi anche

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
