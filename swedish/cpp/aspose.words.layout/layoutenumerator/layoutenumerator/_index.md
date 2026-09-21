---
title: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator konstruktor"
linktitle: "LayoutEnumerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator konstruktor. Initierar en ny instans av den här klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Initierar en ny instans av denna klass.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dokument | const System::SharedPtr\<Aspose::Words::Document\>\& | Ett dokument vars sidlayoutmodell ska enumereras. |
## Anmärkningar


Om sidlayoutmodellen för dokumentet inte har byggts anropar enumeratorn [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) för att bygga den.

När dokumentet uppdateras och en ny sidlayoutmodell skapas, måste en ny enumerator användas för att komma åt den.

## Se även

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
