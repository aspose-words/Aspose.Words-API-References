---
title: "Aspose::Words::Document::get_Frameset metodo"
linktitle: "get_Frameset"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_Frameset metodo. Restituisce un'istanza Frameset se questo documento rappresenta una pagina con frame in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words/document/get_frameset/
---
## Document::get_Frameset method


Restituisce un'istanza [Frameset](./) se questo documento rappresenta una pagina con frame.

```cpp
System::SharedPtr<Aspose::Words::Framesets::Frameset> Aspose::Words::Document::get_Frameset() const
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

* Class [Frameset](../../../aspose.words.framesets/frameset/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
