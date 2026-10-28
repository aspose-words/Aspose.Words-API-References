---
title: Aspose::Words::ImportFormatOptions::set_MergePastedLists method
linktitle: set_MergePastedLists
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::set_MergePastedLists method. Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is false in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words/importformatoptions/set_mergepastedlists/
---
## ImportFormatOptions::set_MergePastedLists method


Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is **false**.

```cpp
void Aspose::Words::ImportFormatOptions::set_MergePastedLists(bool value)
```

## Examples


Shows how to merge lists from a documents.

```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"List item.docx"));
auto dstDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"List destination.docx"));

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
dstDoc->AppendDocument(srcDoc, ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```
## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
