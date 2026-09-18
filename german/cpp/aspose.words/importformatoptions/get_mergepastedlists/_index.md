---
title: "Aspose::Words::ImportFormatOptions::get_MergePastedLists Methode"
linktitle: "get_MergePastedLists"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_MergePastedLists-Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob eingefügte Listen mit den umgebenden Listen zusammengeführt werden. Der Standardwert ist false in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Liest oder setzt einen booleschen Wert, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Beispiele



Zeigt, wie Listen aus einem Dokument zusammengeführt werden.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Setzen Sie die Eigenschaft "MergePastedLists" auf "true", werden eingefügte Listen mit den umgebenden Listen zusammengeführt.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
