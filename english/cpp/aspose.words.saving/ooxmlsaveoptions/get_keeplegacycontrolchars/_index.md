---
title: get_KeepLegacyControlChars
second_title: Aspose.Words for C++ API Reference
description: Keeps original representation of legacy control characters.
type: docs
weight: 40
url: /cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions.get_KeepLegacyControlChars method


Keeps original representation of legacy control characters.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Examples




Shows how to support legacy control characters when converting to .docx. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Legacy control character.doc");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "KeepLegacyControlChars" property to "true" to preserve
// the "ShortDateTime" legacy character while saving.
// Set the "KeepLegacyControlChars" property to "false" to remove
// the "ShortDateTime" legacy character from the output document.
auto so = MakeObject<OoxmlSaveOptions>(SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : String(u"\u001e\f"),
          doc->get_FirstSection()->get_Body()->GetText());
```

