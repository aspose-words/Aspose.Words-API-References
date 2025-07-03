---
title: Aspose::Words::DocumentBase::get_Document method
linktitle: get_Document
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBase::get_Document method. Gets this instance in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Gets this instance.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Examples



Shows how to create simple document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## See Also

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
