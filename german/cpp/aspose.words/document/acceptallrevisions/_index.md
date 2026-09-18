---
title: "Aspose::Words::Document::AcceptAllRevisions Methode"
linktitle: "AcceptAllRevisions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::AcceptAllRevisions Methode. Akzeptiert alle nachverfolgten Änderungen im Dokument in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Akzeptiert alle nachverfolgten Änderungen im Dokument.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Beispiele



Zeigt, wie alle nachverfolgten Änderungen im Dokument akzeptiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bearbeiten Sie das Dokument bei aktivierter Nachverfolgung von Änderungen, um einige Revisionen zu erstellen.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Wir können durch jede Revision iterieren und sie im Rahmen unseres Dokuments akzeptieren oder ablehnen.
// Wenn wir wissen, dass wir jede Revision akzeptieren möchten, können wir dies einfacher tun, indem wir diese Methode aufrufen.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
