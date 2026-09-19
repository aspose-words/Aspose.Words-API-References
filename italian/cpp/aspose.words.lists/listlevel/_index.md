---
title: "Classe Aspose::Words::Lists::ListLevel"
linktitle: "ListLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Lists::ListLevel. Definisce la formattazione per un livello di elenco. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Definisce la formattazione per un livello di elenco. Per saperne di più, visita l'articolo di documentazione [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Crea una forma di pallino immagine per il livello di elenco corrente. |
| [DeletePictureBullet](./deletepicturebullet/)() | Elimina il pallino immagine per il livello di elenco corrente. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Confronta con il [ListLevel](./) specificato. |
| [get_Alignment](./get_alignment/)() const | Ottiene o imposta l'allineamento del numero effettivo dell'elemento dell'elenco. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Ottiene o imposta il formato personalizzato dello stile di numerazione per questo livello di elenco. Per esempio: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Specifica la formattazione dei caratteri utilizzata per l'etichetta dell'elenco. |
| [get_ImageData](./get_imagedata/)() | Restituisce i dati immagine della forma del pallino immagine per il livello di elenco corrente. |
| [get_IsLegal](./get_islegal/)() const | True se il livello converte tutti i numeri ereditati in arabo, false se conserva il loro stile di numerazione. |
| [get_LinkedStyle](./get_linkedstyle/)() | Ottiene o imposta lo stile di paragrafo collegato a questo livello di elenco. |
| [get_NumberFormat](./get_numberformat/)() const | Restituisce o imposta il formato del numero per il livello di elenco. |
| [get_NumberPosition](./get_numberposition/)() const | Restituisce o imposta la posizione (in punti) del numero o del pallino per il livello di elenco. |
| [get_NumberStyle](./get_numberstyle/)() const | Restituisce o imposta lo stile di numerazione per questo livello di elenco. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Imposta o restituisce il livello di elenco che deve apparire prima che il livello di elenco specificato riavvii la numerazione. |
| [get_StartAt](./get_startat/)() | Restituisce o imposta il numero iniziale per questo livello di elenco. |
| [get_TabPosition](./get_tabposition/)() const | Restituisce o imposta la posizione della tabulazione (in punti) per il livello di elenco. |
| [get_TextPosition](./get_textposition/)() const | Restituisce o imposta la posizione (in punti) della seconda riga del testo a capo per il livello di elenco. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Restituisce o imposta il carattere inserito dopo il numero per il livello di elenco. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Restituisce la rappresentazione stringa dell'oggetto [ListLevel](./) per l'indice specificato dell'elemento dell'elenco. I parametri specificano il [NumberStyle](../../aspose.words/numberstyle/) e una stringa di formato opzionale usata quando è specificato [Custom](../../aspose.words/numberstyle/). |
| [GetHashCode](./gethashcode/)() const override | Calcola il codice hash per questo oggetto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Rimuove la tabulazione dal livello di elenco. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Setter per [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | Setter per [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | Setter per [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter per [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | Setter per [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | Setter per [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Setter per [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Setter per [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | Setter per [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | Setter per [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | Setter per [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Setter per [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## Note


Non si creano oggetti di questa classe. Gli oggetti di livello [List](../list/) vengono creati automaticamente quando si crea un elenco. Si accede agli oggetti [ListLevel](./) tramite la collezione [ListLevelCollection](../listlevelcollection/).

Utilizza le proprietà di [ListLevel](./) per specificare la formattazione dell'elenco per i singoli livelli.

## Esempi



Mostra come applicare una formattazione personalizzata dell'elenco ai paragrafi quando si utilizza [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello Microsoft Word e personalizza i primi due livelli dell'elenco.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Questo valore NumberFormat creerà simboli di elenco puntato a forma di stella.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Crea paragrafi e applica entrambi i livelli dell'elenco della nostra formattazione personalizzata a essi.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
