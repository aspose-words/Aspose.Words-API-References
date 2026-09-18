---
title: "Aspose::Words::DocumentBase::get_PageColor Methode"
linktitle: "get_PageColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::get_PageColor Methode. Gibt die Seitenfarbe des Dokuments zurück oder legt sie fest. Diese Eigenschaft ist eine vereinfachte Version von BackgroundShape in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Gibt die Seitenfarbe des Dokuments zurück oder legt sie fest. Diese Eigenschaft ist eine vereinfachte Version von [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Hinweise


Diese Eigenschaft bietet eine einfache Möglichkeit, eine einheitliche Seitenfarbe für das Dokument festzulegen. Das Setzen dieser Eigenschaft erstellt und setzt ein entsprechendes [BackgroundShape](../get_backgroundshape/).

Wenn die Seitenfarbe nicht festgelegt ist (z. B. gibt es keine Hintergrundform im Dokument), wird **Empty** zurückgegeben.

## Beispiele



Zeigt, wie die Hintergrundfarbe für alle Seiten eines Dokuments festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## Siehe auch

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
