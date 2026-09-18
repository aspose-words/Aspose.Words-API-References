---
title: "Aspose::Words::ParagraphCollection::ToArray Methode"
linktitle: "ToArray"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphCollection::ToArray Methode. Kopiert alle Absätze aus der Sammlung in ein neues Array von Absätzen in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Kopiert alle Absätze aus der Sammlung in ein neues Array von Absätzen.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

Ein Array von Absätzen.

## Beispiele



Zeigt, wie man ein Array aus einer [NodeCollection](../../nodecollection/) erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Zeigt, wie man "Hot Remove" verwendet, um einen Knoten während der Aufzählung zu entfernen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Entferne einen Knoten aus der Sammlung mitten in einer Aufzählung.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## Siehe auch

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
