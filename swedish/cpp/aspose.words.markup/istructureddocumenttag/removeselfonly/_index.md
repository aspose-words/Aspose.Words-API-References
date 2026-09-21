---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly method"
linktitle: "RemoveSelfOnly"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly method. Tar bara bort denna SDT-nod själv, men behåller dess innehåll i dokumentträdet i C++."
type: docs
weight: 17500
url: /sv/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
```


## Exempel



Visar hur man tar bort strukturerad dokumenttagg, men behåller innehållet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Denna samling tillhandahåller ett enhetligt gränssnitt för åtkomst till räckvidds- och icke‑räckviddsstrukturerade taggar.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Här kan vi hämta undernoder från det gemensamma gränssnittet för räckvidds- och icke‑räckviddsstrukturerade taggar.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Se även

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
