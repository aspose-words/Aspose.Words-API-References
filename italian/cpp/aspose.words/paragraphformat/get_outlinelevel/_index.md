---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel metodo"
linktitle: "get_OutlineLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel metodo. Specifica il livello di struttura del paragrafo nel documento in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Specifica il livello di struttura del paragrafo nel documento.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Esempi



Mostra come configurare i livelli di contorno dei paragrafi per creare testo comprimibile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ogni paragrafo ha un OutlineLevel, che può essere qualsiasi numero da 1 a 9, o al valore predefinito "BodyText".
// Impostare la proprietà su uno dei valori numerati mostrerà una freccia a sinistra
// all'inizio del paragrafo.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Il livello 1 è il livello più alto. Se c'è un paragrafo con un livello inferiore sotto un paragrafo con un livello superiore,
// comprimere il paragrafo di livello superiore comprimerà il paragrafo di livello inferiore.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Due paragrafi dello stesso livello non si comprimeranno a vicenda,
// e le frecce non comprimono i paragrafi a cui puntano.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// Il valore predefinito "BodyText" è il più basso, che un paragrafo di qualsiasi livello può comprimere.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## Vedi anche

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
