---
title: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator Konstruktor"
linktitle: "LayoutEnumerator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator Konstruktor. Initialisiert eine neue Instanz dieser Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Initialisiert eine neue Instanz dieser Klasse.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Dokument | const System::SharedPtr\<Aspose::Words::Document\>\& | Ein Dokument, dessen Seitenlayoutmodell enumeriert werden soll. |
## Hinweise


Wenn das Seitenlayoutmodell des Dokuments noch nicht erstellt wurde, ruft der Enumerator [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) auf, um es zu erstellen.

Immer wenn das Dokument aktualisiert wird und ein neues Seitenlayoutmodell erstellt wird, muss ein neuer Enumerator verwendet werden, um darauf zuzugreifen.

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
