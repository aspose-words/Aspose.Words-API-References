---
title: get_IgnoreHeaderFooter
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if KeepSourceFormatting mode is used. The default value is true.
type: docs
weight: 27
url: /cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions.get_IgnoreHeaderFooter method


Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if **KeepSourceFormatting** mode is used. The default value is **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Examples




Shows how to specifies ignoring or not source formatting of headers/footers content. 
```cpp
auto dstDoc = MakeObject<Document>(MyDir + u"Document.docx");
auto srcDoc = MakeObject<Document>(MyDir + u"Header and footer types.docx");

auto importFormatOptions = MakeObject<ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(ArtifactsDir + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

