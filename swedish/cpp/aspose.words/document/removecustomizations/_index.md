---
title: "Aspose::Words::Document::RemoveCustomizations method"
linktitle: "RemoveCustomizations"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::RemoveCustomizations method. Tar bort verktygsfälts- och tangentbordskommandomodifieringar från dokumentet i C++."
type: docs
weight: 67750
url: /sv/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Tar bort verktygsfält och anpassade tangentbordskommandon från dokumentet.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Exempel



Visar hur man tar bort verktygsfälts- och tangentbordskommandomodifieringar från dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Ta bort alla anpassade UI‑anpassningar för dokumentet, inklusive anpassade snabbmeny‑poster.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
