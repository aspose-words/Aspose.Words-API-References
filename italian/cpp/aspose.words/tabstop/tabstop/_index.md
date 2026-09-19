---
title: "Aspose::Words::TabStop::TabStop costruttore"
linktitle: "TabStop"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStop::TabStop costruttore. Inizializza una nuova istanza di questa classe in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/tabstop/tabstop/
---
## TabStop::TabStop(double) constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::TabStop::TabStop(double position)
```


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

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStop::TabStop(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::TabStop::TabStop(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double | La posizione della tabulazione in punti. |
| alignment | Aspose::Words::TabAlignment | Un valore [TabAlignment](../../tabalignment/) che specifica l'allineamento del testo a questa tabulazione. |
| leader | Aspose::Words::TabLeader | Un valore [TabLeader](../../tableader/) che specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione. |

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

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
