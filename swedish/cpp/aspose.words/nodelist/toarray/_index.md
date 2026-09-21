---
title: "Aspose::Words::NodeList::ToArray metod"
linktitle: "ToArray"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeList::ToArray metod. Kopierar alla noder från samlingen till en ny nodarray i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Kopierar alla noder från samlingen till en ny nodarray.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

En array av noder.
## Anmärkningar


Du bör inte lägga till/ta bort noder medan du itererar över en samling noder eftersom det ogiltigförklarar iteratorn och kräver uppdateringar för levande samlingar.

För att kunna lägga till/ta bort noder under iteration, använd den här metoden för att kopiera noder till en fast storlek‑array och sedan iterera över arrayen.

## Se även

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
