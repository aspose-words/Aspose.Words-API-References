---
title: "Metodo Aspose::Words::TabStopCollection::Add"
linktitle: "Add"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::TabStopCollection::Add. Aggiunge o sostituisce una tabulazione nella collezione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Aggiunge o sostituisce una tabulazione nella raccolta.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Un oggetto tab stop da aggiungere. |
## Note


Se una tabulazione esiste già nella posizione specificata, viene sostituita.

## Esempi



Mostra come aggiungere tabulazioni personalizzate a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Di seguito sono riportati due modi per aggiungere tabulazioni alla collezione di tabulazioni di un paragrafo tramite la proprietà "ParagraphFormat".
// 1 -  Crea un oggetto "TabStop" e poi aggiungilo alla collezione:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Passa i valori delle proprietà di una nuova tabulazione al metodo "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Aggiungi tabulazioni a 5 cm a tutti i paragrafi.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Ogni carattere \"tab\" sposta il cursore del builder nella posizione della prossima tabulazione.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Vedi anche

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Aggiunge o sostituisce una tabulazione nella raccolta.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| posizione | double | Una posizione (in punti) dove aggiungere la tabulazione. |
| alignment | Aspose::Words::TabAlignment | Un valore [TabAlignment](../../tabalignment/) che specifica l'allineamento del testo alla tabulazione. |
| leader | Aspose::Words::TabLeader | Un valore [TabLeader](../../tableader/) che specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione. |
## Note


Se una tabulazione esiste già nella posizione specificata, viene sostituita.

## Esempi



Mostra come aggiungere tabulazioni personalizzate a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Di seguito sono riportati due modi per aggiungere tabulazioni alla collezione di tabulazioni di un paragrafo tramite la proprietà "ParagraphFormat".
// 1 -  Crea un oggetto "TabStop" e poi aggiungilo alla collezione:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Passa i valori delle proprietà di una nuova tabulazione al metodo "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Aggiungi tabulazioni a 5 cm a tutti i paragrafi.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Ogni carattere \"tab\" sposta il cursore del builder nella posizione della prossima tabulazione.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Vedi anche

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
