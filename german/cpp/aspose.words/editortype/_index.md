---
title: "Aspose::Words::EditorType enum"
linktitle: "EditorType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::EditorType enum. Gibt die Menge möglicher Aliase (oder Bearbeitungsgruppen) an, die als Aliase verwendet werden können, um zu bestimmen, ob dem aktuellen Benutzer das Bearbeiten eines einzelnen, durch einen bearbeitbaren Bereich definierten Bereichs innerhalb eines Dokuments in C++ erlaubt ist."
type: docs
weight: 88000
url: /de/cpp/aspose.words/editortype/
---
## EditorType enum


Gibt die Menge möglicher Aliase (oder Bearbeitungsgruppen) an, die als Aliase verwendet werden können, um zu bestimmen, ob dem aktuellen Benutzer das Bearbeiten eines einzelnen Bereichs erlaubt ist, der durch einen editierbaren Bereich innerhalb eines Dokuments definiert ist.

```cpp
enum class EditorType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Nicht angegeben | 0 | Bedeutet, dass der Editor-Typ nicht angegeben ist. |
| Administratoren | 1 | Gibt an, dass Benutzer, die der Gruppe Administratoren zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Mitwirkende | 2 | Gibt an, dass Benutzer, die der Gruppe Mitwirkende zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Aktuell | 3 | Gibt an, dass Benutzer, die der Gruppe Aktuell zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Redakteure | 4 | Gibt an, dass Benutzer, die der Gruppe Redakteure zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Alle | 5 | Gibt an, dass allen Benutzern, die das Dokument öffnen, das Bearbeiten bearbeitbarer Bereiche mit diesem Bearbeitungstyp erlaubt ist, wenn der Dokumentenschutz aktiviert ist. |
| Keine | 6 | Gibt an, dass keinem der Benutzer, die das Dokument öffnen, das Bearbeiten bearbeitbarer Bereiche mit diesem Bearbeitungstyp erlaubt ist, wenn der Dokumentenschutz aktiviert ist. |
| Eigentümer | 7 | Gibt an, dass Benutzern, die der Gruppe Eigentümer zugeordnet sind, das Bearbeiten bearbeitbarer Bereiche mit diesem Bearbeitungstyp erlaubt ist, wenn der Dokumentenschutz aktiviert ist. |
| Default | n/a | Wie [Unspecified](./). |

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
