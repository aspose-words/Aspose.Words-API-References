---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method. Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo. Il valore predefinito è false in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Esempi



Mostra come rimuovere un paragrafo da una cella di tabella con una tabella annidata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea una tabella con paragrafo e tabella interna nella prima cella.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// Quando l'opzione seguente è impostata su 'true', Aspose.Words rimuoverà il testo del paragrafo
// completamente insieme al segno di paragrafo. Altrimenti, Aspose.Words imiterà Word e rimuoverà
// solo il testo del paragrafo e lascerà intatto il segno di paragrafo (quando una tabella segue il testo).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
