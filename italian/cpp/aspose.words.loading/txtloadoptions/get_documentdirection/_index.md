---
title: "Metodo Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection"
linktitle: "get_DocumentDirection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection. Ottiene o imposta la direzione del documento. Il valore predefinito è LeftToRight in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


Ottiene o imposta la direzione del documento. Il valore predefinito è [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


## Esempi



Mostra come rilevare la direzione del testo di un documento di testo semplice.
```cpp
// Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo semplice.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Imposta la proprietà "DocumentDirection" su "DocumentDirection.Auto" per rilevare automaticamente
// la direzione di ogni paragrafo di testo che Aspose.Words carica dal testo semplice.
// La proprietà "Bidi" di ogni paragrafo memorizzerà la sua direzione.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Rileva il testo ebraico come da destra a sinistra.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Rileva il testo inglese come da destra a sinistra.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Vedi anche

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
