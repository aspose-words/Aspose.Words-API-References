---
title: "Aspose::Words::Document::Clone metodo"
linktitle: "Clone"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::Clone metodo. Esegue una copia profonda del Document in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/document/clone/
---
## Document::Clone method


Esegue una copia profonda del [Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

Il documento clonato.

## Esempi



Mostra come clonare in profondità un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Il clonaggio produrrà un nuovo documento con gli stessi contenuti dell'originale,
// ma con una copia unica di ciascuno dei nodi del documento originale.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## Vedi anche

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
