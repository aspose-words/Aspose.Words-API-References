---
title: "Aspose::Words::ParagraphFormat::get_Bidi metodo"
linktitle: "get_Bidi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_Bidi metodo. Ottiene o imposta se questo è un paragrafo da destra a sinistra in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Ottiene o imposta se questo è un paragrafo da destra a sinistra.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Note


Quando **true**, le run e gli altri oggetti inline in questo paragrafo sono disposti da destra a sinistra.

## Esempi



Mostra come creare elenchi compatibili con lingue da destra a sinistra usando i campi BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il campo BIDIOUTLINE numera i paragrafi come i campi AUTONUM/LISTNUM,
// ma è visibile solo quando è abilitata una lingua di editing da destra a sinistra, come ebraico o arabo.
// Il campo seguente visualizzerà ".1", l'equivalente RTL del numero di elenco "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Aggiungi altri due campi BIDIOUTLINE, che visualizzeranno ".2" e ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Imposta l'allineamento orizzontale del testo per ogni paragrafo nel documento su RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Se abilitiamo una lingua di editing da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno i numeri.
// Altrimenti, visualizzeranno "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
