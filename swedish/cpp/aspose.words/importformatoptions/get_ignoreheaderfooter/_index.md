---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter metod"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter metod. Hämtar eller anger ett booleskt värde som specificerar att källformatering av rubriker/fotnoter-innehåll ignoreras om läget KeepSourceFormatting används. Standardvärdet är true i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Hämtar eller anger ett booleskt värde som specificerar att källformatering av rubriker/fotnoter-innehåll ignoreras om [KeepSourceFormatting](../../importformatmode/) läget används. Standardvärdet är **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Exempel



Visar hur man anger att källformatering av rubriker/fotnoter-innehåll ska ignoreras eller inte.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Om 'IgnoreHeaderFooter' är false så används den ursprungliga formateringen för rubrik/fotnot-innehåll
// från "Header and footer types.docx" kommer att användas.
// Om 'IgnoreHeaderFooter' är true så används formateringen för rubrik/fotnot-innehåll
// från "Document.docx" kommer att användas.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
