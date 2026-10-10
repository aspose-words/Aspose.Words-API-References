---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText metod"
linktitle: "get_ShowHiddenText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText metod. Hämtar eller anger indikation på om dold text i dokumentet renderas. Standard är falskt i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Hämtar eller sätter indikation på om dold text i dokumentet renderas. Standard är **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Exempel



Visar hur man döljer text i ett renderat utdata-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga dold text och ange sedan om vi vill utesluta den från ett renderat dokument.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## Se även

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
