---
title: Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks method
linktitle: get_ForcePageBreaks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks method. Allows to specify whether the page breaks should be preserved during export. The default value is false in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Allows to specify whether the page breaks should be preserved during export. The default value is **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Examples



Shows how to specify whether to preserve page breaks when exporting a document to plaintext. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save"
// method to modify how we save the document to plaintext.
auto saveOptions = MakeObject<TxtSaveOptions>();

// The Aspose.Words "Document" objects have page breaks, just like Microsoft Word documents.
// Save formats such as ".txt" are one continuous body of text without page breaks.
// Set the "ForcePageBreaks" property to "true" to preserve all page breaks in the form of '\f' characters.
// Set the "ForcePageBreaks" property to "false" to discard all page breaks.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(ArtifactsDir + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// If we load a plaintext document with page breaks,
// the "Document" object will use them to split the body into pages.
doc = MakeObject<Document>(ArtifactsDir + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## See Also

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
