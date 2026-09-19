---
title: "Classe Aspose::Words::Lists::ListLabel"
linktitle: "ListLabel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Lists::ListLabel. Definisce le proprietà specifiche di un'etichetta di elenco. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.lists/listlabel/
---
## ListLabel class


Definisce le proprietà specifiche di un'etichetta di elenco. Per saperne di più, visita l'articolo di documentazione [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLabel : public Aspose::Words::IRunAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Font](./get_font/)() | Ottiene il carattere dell'etichetta di elenco. |
| [get_LabelString](./get_labelstring/)() | Ottiene una rappresentazione stringa dell'etichetta di elenco. |
| [get_LabelValue](./get_labelvalue/)() | Ottiene un valore numerico per questa etichetta. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
