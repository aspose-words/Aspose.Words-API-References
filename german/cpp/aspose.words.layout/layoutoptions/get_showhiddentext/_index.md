---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText Methode"
linktitle: "get_ShowHiddenText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText Methode. Ermittelt oder legt fest, ob versteckter Text im Dokument gerendert wird. Standardwert ist false in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Liest oder schreibt die Angabe, ob versteckter Text im Dokument dargestellt wird. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Beispiele



Zeigt, wie man Text in einem gerenderten Ausgabedokument ausblendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie versteckten Text ein und geben Sie dann an, ob wir ihn aus einem gerenderten Dokument weglassen möchten.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## Siehe auch

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
