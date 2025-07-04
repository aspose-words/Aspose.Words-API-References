---
title: Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter method
linktitle: get_IgnoreHeaderFooter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter method. Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if KeepSourceFormatting mode is used. The default value is true in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if [KeepSourceFormatting](../../importformatmode/) mode is used. The default value is **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Examples



Shows how to specifies ignoring or not source formatting of headers/footers content. 
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
// from "Header and footer types.docx" will be used.
// If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
// from "Document.docx" will be used.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
