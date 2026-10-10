---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StoryType enum. Il testo di un documento Word è memorizzato in storie. StoryType identifica una storia in C++."
type: docs
weight: 117000
url: /it/cpp/aspose.words/storytype/
---
## StoryType enum


Il testo di un documento Word è memorizzato in storie. [StoryType](./) identifica una storia.

```cpp
enum class StoryType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Valore predefinito. Non esiste tale storia nel documento. |
| MainText | 1 | Contiene il testo principale del documento, rappresentato da [Body](../body/). |
| Footnotes | 2 | Contiene il testo della nota a piè di pagina, rappresentato da [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Contiene il testo delle note finali, rappresentato da [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Contiene i commenti del documento (annotazioni), rappresentati da [Comment](../comment/). |
| Textbox | 5 | Contiene il testo di forme o caselle di testo, rappresentato da [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Contiene il testo dell'intestazione delle pagine pari, rappresentato da [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Contiene il testo dell'intestazione primaria. Quando l'intestazione è diversa per le pagine dispari e pari, contiene il testo dell'intestazione delle pagine dispari. Rappresentato da [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Contiene il testo del piè di pagina delle pagine pari, rappresentato da [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Contiene il testo del piè di pagina primario. Quando il piè di pagina è diverso per le pagine dispari e pari, contiene il testo del piè di pagina delle pagine dispari. Rappresentato da [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Contiene il testo dell'intestazione della prima pagina, rappresentato da [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Contiene il testo del piè di pagina della prima pagina, rappresentato da [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Contiene il testo del separatore della nota a piè di pagina. |
| FootnoteContinuationSeparator | 13 | Contiene il testo del separatore di continuazione della nota a piè di pagina. |
| FootnoteContinuationNotice | 14 | Contiene il testo del separatore di avviso di continuazione della nota a piè di pagina. |
| EndnoteSeparator | 15 | Contiene il testo del separatore della nota finale. |
| EndnoteContinuationSeparator | 16 | Contiene il testo del separatore di continuazione della nota finale. |
| EndnoteContinuationNotice | 17 | Contiene il testo del separatore di avviso di continuazione della nota finale. |


## Esempi



Mostra come rimuovere tutte le forme da un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Usa un DocumentBuilder per inserire una forma. Questa è una forma inline,
// che ha un Paragraph genitore, che è un nodo figlio del Body della prima sezione.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Possiamo eliminare tutte le forme dai paragrafi figli di questo Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
