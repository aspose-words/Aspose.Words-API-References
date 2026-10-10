---
title: "Aspose::Words::Framesets::FramesetCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Framesets::FramesetCollection::idx_get metodo. Ottiene un frame o una pagina di frame all'indice specificato in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.framesets/framesetcollection/idx_get/
---
## FramesetCollection::idx_get method


Ottiene un frame o una pagina di frame all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Framesets::Frameset> Aspose::Words::Framesets::FramesetCollection::idx_get(int32_t index)
```


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

* Class [Frameset](../../frameset/)
* Class [FramesetCollection](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
