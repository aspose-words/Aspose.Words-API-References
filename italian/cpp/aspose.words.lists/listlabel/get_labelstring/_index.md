---
title: "Aspose::Words::Lists::ListLabel::get_LabelString metodo"
linktitle: "get_LabelString"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListLabel::get_LabelString metodo. Ottiene una rappresentazione stringa dell'etichetta dell'elenco in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.lists/listlabel/get_labelstring/
---
## ListLabel::get_LabelString method


Ottiene una rappresentazione stringa dell'etichetta di elenco.

```cpp
System::String Aspose::Words::Lists::ListLabel::get_LabelString()
```


## Esempi



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

## Vedi anche

* Class [ListLabel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
