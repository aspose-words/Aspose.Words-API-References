---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::JustificationMode enum. Gibt die Zeichenabstandsanpassung für ein Dokument an. Der Standardwert ist Expand in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Gibt die Zeichenabstandsanpassung für ein Dokument an. Der Standardwert ist **Expand**.

```cpp
enum class JustificationMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Expand | 0 | Zeichenabstand nicht komprimieren. |
| Compress | 1 | Zeichenabstand komprimieren. |
| CompressKana | 2 | Komprimieren nach den Regeln der Kana-Silbenschriften, Hiragana und Katakana. |


## Beispiele



Zeigt, wie die Zeichenabstandskontrolle verwaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
