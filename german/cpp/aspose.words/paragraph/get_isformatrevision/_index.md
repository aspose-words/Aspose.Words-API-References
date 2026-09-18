---
title: "Aspose::Words::Paragraph::get_IsFormatRevision method"
linktitle: "get_IsFormatRevision"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::get_IsFormatRevision method. Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Nachverfolgung von Änderungen in C++ aktiviert war."
type: docs
weight: 12000
url: /de/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Beispiele



Zeigt, wie man prüft, ob ein Absatz eine Formatrevision ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Dieser Absatz ist eine "Format"‑Revision, die auftritt, wenn wir die Formatierung des bestehenden Textes ändern
// während wir Revisionen in Microsoft Word über "Review" -> "Track changes" verfolgen.
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## Siehe auch

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
