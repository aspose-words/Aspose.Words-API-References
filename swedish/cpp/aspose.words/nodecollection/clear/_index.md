---
title: "Aspose::Words::NodeCollection::Clear‑metod"
linktitle: "Clear"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::Clear‑metod. Tar bort alla noder från denna samling och från dokumentet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Tar bort alla noder från denna samling och från dokumentet.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Exempel



Visar hur man tar bort alla sektioner från ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Det här dokumentet har en sektion med några undernoder som innehåller och visar hela dokumentets innehåll.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Rensa samlingen av sektioner, vilket kommer att ta bort alla dokumentets underordnade element.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## Se även

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
