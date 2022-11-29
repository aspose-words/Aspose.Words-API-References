---
title: get_CreateNoteHyperlinks
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is false.
type: docs
weight: 66
url: /cpp/aspose.words.saving/pdfsaveoptions/get_createnotehyperlinks/
---
## PdfSaveOptions::get_CreateNoteHyperlinks method


Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CreateNoteHyperlinks() const
```


## Examples



Shows how to make footnotes and endnotes function as hyperlinks. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Footnotes and endnotes.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "CreateNoteHyperlinks" property to "true" to turn all footnote/endnote symbols
// in the text act as links that, upon clicking, take us to their respective footnotes/endnotes.
// Set the "CreateNoteHyperlinks" property to "false" not to have footnote/endnote symbols link to anything.
options->set_CreateNoteHyperlinks(createNoteHyperlinks);

doc->Save(ArtifactsDir + u"PdfSaveOptions.NoteHyperlinks.pdf", options);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
