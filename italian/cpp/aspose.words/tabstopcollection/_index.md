---
title: "Aspose::Words::TabStopCollection classe"
linktitle: "TabStopCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStopCollection classe. Una raccolta di oggetti TabStop che rappresentano tabulazioni personalizzate per un paragrafo o uno stile. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 69000
url: /it/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


Una raccolta di oggetti [TabStop](../tabstop/) che rappresentano tabulazioni personalizzate per un paragrafo o uno stile. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Aggiunge o sostituisce una tabulazione nella raccolta. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Aggiunge o sostituisce una tabulazione nella raccolta. |
| [After](./after/)(double) | Restituisce la prima tabulazione a destra della posizione specificata. |
| [Before](./before/)(double) | Restituisce la prima tabulazione a sinistra della posizione specificata. |
| [Clear](./clear/)() | Elimina tutte le posizioni delle tabulazioni. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Determina se la [TabStopCollection](./) specificata è uguale in valore alla [TabStopCollection](./) corrente. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_Count](./get_count/)() | Restituisce il numero di tabulazioni nella raccolta. |
| [GetHashCode](./gethashcode/)() const override | Funziona come funzione hash per questo tipo. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Restituisce l'indice di una tabulazione con la posizione specificata in punti. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Restituisce la posizione (in punti) della tabulazione all'indice specificato. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce una tabulazione all'indice fornito. |
| [idx_get](./idx_get/)(double) | Restituisce una tabulazione alla posizione specificata. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Rimuove una tabulazione all'indice specificato dalla raccolta. |
| [RemoveByPosition](./removebyposition/)(double) | Rimuove una tabulazione alla posizione specificata dalla raccolta. |
| static [Type](./type/)() |  |
## Note


Nei documenti Microsoft Word, una tabulazione può essere definita nelle proprietà di uno stile di paragrafo o direttamente nelle proprietà di un paragrafo. Uno stile può basarsi su un altro stile. Pertanto, l'insieme completo di tabulazioni per un determinato oggetto è una combinazione di tabulazioni definite direttamente su questo oggetto e di tabulazioni ereditate dagli stili genitore.

In Aspose.Words, quando ottieni una [TabStopCollection](./) per un paragrafo o uno stile, contiene solo le tabulazioni personalizzate definite direttamente per quel paragrafo o stile. La raccolta non include le tabulazioni definite negli stili genitore o le tabulazioni predefinite.

## Esempi



Mostra come lavorare con la raccolta di tabulazioni di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 punti corrispondono a un \"pollice\" sulla righello delle tabulazioni di Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Ogni carattere \"tab\" sposta il cursore del builder nella posizione della prossima tabulazione.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Ogni paragrafo ottiene la sua raccolta di tabulazioni, che clona i suoi valori dalla raccolta di tabulazioni del document builder.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Una raccolta di tabulazioni può indicarci le TabStop prima e dopo determinate posizioni.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Possiamo cancellare la raccolta di tabulazioni di un paragrafo per tornare al comportamento di tabulazione predefinito.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Vedi anche

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
