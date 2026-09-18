---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks Methode"
linktitle: "get_ShowParagraphMarks"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks Methode. Gibt an, ob Absatzmarken gerendert werden, oder legt dies fest. Der Standardwert ist false in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Liest oder schreibt die Angabe, ob Absatzmarken dargestellt werden. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Beispiele



Zeigt, wie man Absatzmarken in einem gerenderten Ausgabedokument anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige Absätze hinzu und aktivieren Sie dann Absatzmarken, um das Ende der Absätze anzuzeigen
// mit einem Pilcrow‑Symbol (¶), wenn wir das Dokument rendern.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## Siehe auch

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
