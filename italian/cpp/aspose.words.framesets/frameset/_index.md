---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Framesets::Frameset class. Rappresenta una pagina di frame o un singolo frame su una pagina di frame. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Rappresenta una pagina di frame o un singolo frame su una pagina di frame. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Frameset : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Ottiene la collezione di frame figlio e pagine di frame. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Ottiene o imposta l'URL della pagina web o il nome file del documento da visualizzare in questo frame. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Ottiene o imposta un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [FrameDefaultUrl](./get_framedefaulturl/) è una risorsa esterna a cui il frame è collegato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Impostatore per [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Impostatore per [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come accedere ai frame nella pagina.
```cpp
// Il documento contiene diversi frame con collegamenti ad altri documenti.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Possiamo verificare l'URL predefinito (un URL di pagina web o documento locale) o se il frame è una risorsa esterna.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Modifica le proprietà di uno dei nostri frame.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## Vedi anche

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
