---
title: "Aspose::Words::DropCapPosition enum"
linktitle: "DropCapPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DropCapPosition enum. Specifica la posizione per un testo con capilettera in C++."
type: docs
weight: 87000
url: /it/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Specifica la posizione per un capolettera.

```cpp
enum class DropCapPosition
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Il paragrafo non ha una capilettera. |
| Normale | 1 | La capilettera è posizionata all'interno del margine del testo nel paragrafo di ancoraggio. |
| Margine | 2 | La capilettera è posizionata al di fuori del margine del testo nel paragrafo di ancoraggio. |


## Esempi



Mostra come creare una capilettera.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un paragrafo con una lettera grande con cui il testo nei secondi e terzi paragrafi inizia.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Attualmente, i secondi e terzi paragrafi appariranno sotto il primo.
// Possiamo convertire il primo paragrafo in una capilettera per gli altri paragrafi tramite il suo oggetto "ParagraphFormat".
// Imposta la proprietà "DropCapPosition" su "DropCapPosition.Margin" per posizionare la capilettera
// al di fuori del margine sinistro della pagina se il nostro testo è da sinistra a destra.
// Imposta la proprietà "DropCapPosition" su "DropCapPosition.Normal" per posizionare la capilettera all'interno dei margini della pagina
// e per avvolgere il resto del testo attorno ad essa.
// "DropCapPosition.None" è lo stato predefinito per tutti i paragrafi.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
