---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::RevisionGroup. Rappresenta un gruppo di oggetti Revision sequenziali. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 54000
url: /it/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Rappresenta un gruppo di oggetti [Revision](../revision/) sequenziali. Per saperne di più, visita l'articolo di documentazione [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Author](./get_author/)() | Ottiene l'autore di questo gruppo di revisioni. |
| [get_RevisionType](./get_revisiontype/)() | Ottiene il tipo di revisioni incluse in questo gruppo. |
| [get_Text](./get_text/)() | Restituisce il testo inserito/eliminato/spostato o la descrizione della modifica di formato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come stampare le informazioni su un gruppo di revisioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
