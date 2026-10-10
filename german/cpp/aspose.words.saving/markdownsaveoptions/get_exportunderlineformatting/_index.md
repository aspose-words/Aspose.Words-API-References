---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting Methode"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob die Unterstreichungs‑Textformatierung als Sequenz von zwei Plus‑Zeichen \"++\" exportiert werden soll. Der Standardwert ist false in C++."
type: docs
weight: 3500
url: /de/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Liest oder setzt einen booleschen Wert, der angibt, ob Unterstreichungs-Textformatierung als Folge von zwei Pluszeichen \"++\" exportiert werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Beispiele



Zeigt, wie Unterstreichungsformatierung als ++ exportiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## Siehe auch

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
