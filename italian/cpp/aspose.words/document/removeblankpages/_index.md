---
title: "Metodo Aspose::Words::Document::RemoveBlankPages"
linktitle: "RemoveBlankPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::RemoveBlankPages. Rimuove le pagine vuote dal documento in C++."
type: docs
weight: 67500
url: /it/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Rimuove le pagine vuote dal documento.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

L'elenco dei numeri di pagina è stato considerato vuoto e rimosso.

## Esempi



Mostra come rimuovere le pagine vuote dal documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
