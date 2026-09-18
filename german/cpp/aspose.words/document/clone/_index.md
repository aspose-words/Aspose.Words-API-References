---
title: "Aspose::Words::Document::Clone Methode"
linktitle: "Klonen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::Clone Methode. Führt eine tiefe Kopie des Document in C++ aus."
type: docs
weight: 7000
url: /de/cpp/aspose.words/document/clone/
---
## Document::Clone method


Führt eine tiefe Kopie des [Document](../) aus.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

Das geklonte Dokument.

## Beispiele



Zeigt, wie man ein Dokument tief klont.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Das Klonen erzeugt ein neues Dokument mit demselben Inhalt wie das Original,
// jedoch mit einer eindeutigen Kopie jedes Knotens des Originaldokuments.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## Siehe auch

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
