---
title: "Aspose::Words::ParagraphCollection::ToArray metodo"
linktitle: "ToArray"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphCollection::ToArray metodo. Copia tutti i paragrafi dalla collezione in un nuovo array di paragrafi in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Copia tutti i paragrafi dalla raccolta in un nuovo array di paragrafi.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

Un array di paragrafi.

## Esempi



Mostra come creare un array da una [NodeCollection](../../nodecollection/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Mostra come usare "hot remove" per rimuovere un nodo durante l'enumerazione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Rimuovi un nodo dalla collezione nel mezzo di un'enumerazione.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## Vedi anche

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
