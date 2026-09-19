---
title: "Aspose::Words::Paragraph::get_ListLabel metodo"
linktitle: "get_ListLabel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_ListLabel metodo. Ottiene un oggetto ListLabel che fornisce l'accesso al valore di numerazione dell'elenco e alla formattazione per questo paragrafo in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/paragraph/get_listlabel/
---
## Paragraph::get_ListLabel method


Ottiene un oggetto [ListLabel](./) che fornisce l'accesso al valore di numerazione dell'elenco e alla formattazione per questo paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListLabel> Aspose::Words::Paragraph::get_ListLabel()
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

* Class [ListLabel](../../../aspose.words.lists/listlabel/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
