---
title: "Metodo Aspose::Words::Lists::ListFormat::RemoveNumbers"
linktitle: "RemoveNumbers"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Lists::ListFormat::RemoveNumbers. Rimuove numeri o punti elenco dal paragrafo corrente e imposta il livello dell'elenco a zero in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.lists/listformat/removenumbers/
---
## ListFormat::RemoveNumbers method


Rimuove numeri o punti elenco dal paragrafo corrente e imposta il livello dell'elenco a zero.

```cpp
void Aspose::Words::Lists::ListFormat::RemoveNumbers()
```

## Note


Chiamare questo metodo è equivalente a impostare la proprietà [List](../get_list/) su **null**.

## Esempi



Mostra come creare liste puntate e numerate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Di seguito sono due tipi di liste che possiamo creare con un document builder.
// 1 -  Una lista puntata:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Termina la lista puntata.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Una lista numerata:
// Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder->get_ListFormat()->ApplyNumberDefault();

// Questo paragrafo è il primo elemento. Il primo elemento di una lista numerata avrà un "1." come simbolo dell'elemento della lista.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Chiama il metodo "ListIndent" per aumentare il livello corrente dell'elenco,
// che avvierà un nuovo elenco autonomo, con un'indentazione più profonda, all'elemento corrente del primo livello dell'elenco.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Questi sono i primi tre elementi dell'elenco del secondo livello, che manterranno un conteggio
// indipendente dal conteggio del primo livello dell'elenco. Secondo il formato corrente dell'elenco,
// avranno i simboli "a.", "b.", e "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Chiama il metodo "ListOutdent" per tornare al livello precedente dell'elenco.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Questi due paragrafi continueranno il conteggio del primo livello dell'elenco.
// Questi elementi avranno i simboli "2.", e "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Se aumentiamo il livello dell'elenco a un livello al quale abbiamo già aggiunto elementi in precedenza,
// l'elenco annidato sarà separato dal precedente, e la sua numerazione inizierà dall'inizio.
// Questi elementi dell'elenco avranno i simboli "a.", "b.", "c.", "d.", e "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Riduci nuovamente il livello dell'elenco.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Termina l'elenco numerato.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


Mostra come rimuovere la formattazione dell'elenco da tutti i paragrafi nel testo principale di una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);
ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(paras))
{
    paragraph->get_ListFormat()->RemoveNumbers();
}

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## Vedi anche

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
