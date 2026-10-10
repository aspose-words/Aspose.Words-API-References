---
title: "Aspose::Words::Lists::ListLevel::get_LinkedStyle metodo"
linktitle: "get_LinkedStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListLevel::get_LinkedStyle metodo. Ottiene o imposta lo stile di paragrafo collegato a questo livello dell'elenco in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.lists/listlevel/get_linkedstyle/
---
## ListLevel::get_LinkedStyle method


Ottiene o imposta lo stile di paragrafo collegato a questo livello di elenco.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::ListLevel::get_LinkedStyle()
```

## Note


Questa proprietà è **null** quando il livello dell'elenco non è collegato a uno stile di paragrafo. Questa proprietà può essere impostata su **null**.

## Esempi



Mostra modi avanzati per personalizzare le etichette degli elenchi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Le etichette di livello 1 saranno formattate secondo lo stile di paragrafo \"Heading 1\" e avranno un prefisso.
// Queste avranno l'aspetto di \"Appendix A\", \"Appendix B\"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Le etichette di livello 2 visualizzeranno i numeri correnti del primo e del secondo livello di elenco e avranno zeri iniziali.
// Se il primo livello di elenco è a 1, le etichette di elenco risultanti avranno l'aspetto di \"Section (1.01)\", \"Section (1.02)\"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Nota che il livello superiore utilizza la numerazione UppercaseLetter.
// Possiamo impostare la proprietà \"IsLegal\" per utilizzare numeri arabi per i livelli di elenco superiori.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Le etichette di livello 3 saranno numeri romani maiuscoli con un prefisso e un suffisso e verranno riavviate per ogni elemento di livello 1 dell'elenco.
// Queste etichette di elenco avranno l'aspetto di \"-I-\", \"-II-\"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Rendi in grassetto le etichette di tutti i livelli di elenco.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Applica la formattazione dell'elenco al paragrafo corrente.
builder->get_ListFormat()->set_List(list);

// Crea elementi di elenco che visualizzeranno tutti e tre i nostri livelli di elenco.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## Vedi anche

* Class [Style](../../../aspose.words/style/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
