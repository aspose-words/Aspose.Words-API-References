---
title: "Aspose::Words::Fields::FieldShape::get_Text metodo"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldShape::get_Text metodo. Ottiene o imposta il testo da recuperare in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Ottiene o imposta il testo da recuperare.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


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


Mostra come alcuni campi più vecchi di Microsoft Word, come SHAPE e EMBED, vengono gestiti durante il caricamento.
```cpp
// Apri un documento creato in Microsoft Word 2003.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Se apriamo il documento Word e premiamo Alt+F9, vedremo un campo SHAPE e un campo EMBED.
// Un campo SHAPE è l'ancora/tela per un oggetto AutoShape con lo stile di avvolgimento "In linea con il testo" abilitato.
// Un campo EMBED ha la stessa funzione, ma per un oggetto incorporato,
// come un foglio di calcolo da un documento Excel esterno.
// Tuttavia, questi campi non appariranno nella raccolta Fields del documento.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Questi campi sono supportati solo dalle versioni più vecchie di Microsoft Word.
// Il processo di caricamento del documento convertirà questi campi in oggetti Shape,
// che possiamo accedere nella raccolta di nodi del documento.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// Il primo nodo Shape corrisponde al campo SHAPE nel documento di input,
// che è la tela in linea per l'AutoShape.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// Il secondo nodo Shape è l'AutoShape stessa.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Il terzo Shape è quello che era il campo EMBED che conteneva il foglio di calcolo esterno.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## Vedi anche

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
