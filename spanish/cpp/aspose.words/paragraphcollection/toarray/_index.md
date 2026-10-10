---
title: "Aspose::Words::ParagraphCollection::ToArray método"
linktitle: "ToArray"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphCollection::ToArray método. Copia todos los párrafos de la colección a una nueva matriz de párrafos en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Copia todos los párrafos de la colección a una nueva matriz de párrafos.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

Una matriz de párrafos.

## Ejemplos



Muestra cómo crear una matriz a partir de una [NodeCollection](../../nodecollection/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Muestra cómo usar "hot remove" para eliminar un nodo durante la enumeración.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Elimina un nodo de la colección en medio de una enumeración.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## Ver también

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
