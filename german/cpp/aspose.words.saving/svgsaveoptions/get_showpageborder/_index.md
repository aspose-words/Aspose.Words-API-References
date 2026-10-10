---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder Methode"
linktitle: "get_ShowPageBorder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder Methode. Steuert, ob dem Seitenumriss ein Rahmen hinzugefügt wird. Standard ist true in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Steuert, ob dem Seitenumriss ein Rahmen hinzugefügt wird. Standard ist **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
```


## Beispiele



Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines .docx-Dokuments in .svg nachgeahmt werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Konfigurieren Sie das SvgSaveOptions-Objekt, um ohne Seitenränder oder auswählbaren Text zu speichern.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Siehe auch

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
