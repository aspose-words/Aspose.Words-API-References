---
title: get_MergePastedLists
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is false.
type: docs
weight: 92
url: /cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Examples



Shows how to merge lists from a documents. 
```cpp
auto srcDoc = MakeObject<Document>(MyDir + u"List item.docx");
auto dstDoc = MakeObject<Document>(MyDir + u"List destination.docx");

auto options = MakeObject<ImportFormatOptions>();
options->set_MergePastedLists(true);

// Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
dstDoc->AppendDocument(srcDoc, ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(ArtifactsDir + u"Document.MergePastedLists.docx");
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
