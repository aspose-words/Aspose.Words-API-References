---
title: "Metodo Aspose::Words::Node::set_CustomNodeId"
linktitle: "ToString"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::ToString. Esporta il contenuto del nodo in una stringa nel formato specificato in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


Esporta il contenuto del nodo in una stringa nel formato specificato.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

Il contenuto del nodo nel formato specificato.

## Esempi



Mostra la differenza tra la chiamata dei metodi GetText e ToString su un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText recupererà il testo visibile così come i codici di campo e i caratteri speciali.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString ci fornirà l'aspetto del documento se salvato nel formato di salvataggio specificato.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Mostra come estrarre le etichette di elenco di tutti i paragrafi che sono elementi di elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Trova se abbiamo l'elenco del paragrafo. Nel nostro documento, il nostro elenco utilizza numeri arabi semplici,
// che iniziano da tre e terminano a sei.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Questo è il testo che otteniamo quando esportiamo questo nodo in formato testo.
    // Questa uscita di testo ometterà le etichette di elenco. Rimuovi eventuali caratteri di formattazione del paragrafo.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Questo ottiene la posizione del paragrafo nel livello corrente dell'elenco. Se abbiamo un elenco con più livelli,
    // ci dirà qual è la sua posizione in quel livello.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Combinali insieme per includere l'etichetta di elenco con il testo nell'output.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```


Esporta il contenuto di un nodo in una stringa nel formato HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Quando chiamiamo il metodo ToString usando la sovraccarico html di SaveFormat,
// converte il contenuto del nodo nella sua rappresentazione HTML grezza.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Possiamo anche modificare il risultato di questa conversione usando un oggetto SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Vedi anche

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Specifica le opzioni che controllano come il nodo viene salvato. |

### ReturnValue

Il contenuto del nodo nel formato specificato.

## Esempi



Esporta il contenuto di un nodo in una stringa nel formato HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Quando chiamiamo il metodo ToString usando la sovraccarico html di SaveFormat,
// converte il contenuto del nodo nella sua rappresentazione HTML grezza.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Possiamo anche modificare il risultato di questa conversione usando un oggetto SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Vedi anche

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
