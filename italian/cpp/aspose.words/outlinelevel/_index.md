---
title: "Enum Aspose::Words::OutlineLevel"
linktitle: "OutlineLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::OutlineLevel. Specifica il livello di struttura di un paragrafo nel documento in C++."
type: docs
weight: 105000
url: /it/cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


Specifica il livello di struttura di un paragrafo nel documento.

```cpp
enum class OutlineLevel
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Level1 | 0 | Il paragrafo è al livello di struttura 1 (livello più alto). |
| Livello2 | 1 | Il paragrafo è al livello di contorno 2. |
| Livello3 | 2 | Il paragrafo è al livello di contorno 3. |
| Livello4 | 3 | Il paragrafo è al livello di contorno 4. |
| Livello5 | 4 | Il paragrafo è al livello di contorno 5. |
| Livello6 | 5 | Il paragrafo è al livello di contorno 6. |
| Livello7 | 6 | Il paragrafo è al livello di contorno 7. |
| Livello8 | 7 | Il paragrafo è al livello di contorno 8. |
| Livello9 | 8 | Il paragrafo è al livello di contorno 9. |
| BodyText | 9 | Il paragrafo è al livello del testo principale. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
