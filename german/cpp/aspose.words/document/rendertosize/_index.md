---
title: "Aspose::Words::Document::RenderToSize Methode"
linktitle: "RenderToSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::RenderToSize Methode. Rendert eine Dokumentseite in ein Graphics‑Objekt auf eine angegebene Größe in C++."
type: docs
weight: 71000
url: /de/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Rendert eine Dokumentseite in ein **Graphics**-Objekt mit einer angegebenen Größe.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | int32_t | Der 0-basierte Seitenindex. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Das Objekt, in das gerendert werden soll. |
| x | float | Die X‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| y | float | Die Y‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| Breite | float | Die maximale Breite (in Welteinheiten), die von der gerenderten Seite eingenommen werden kann. |
| Höhe | float | Die maximale Höhe (in Welteinheiten), die von der gerenderten Seite eingenommen werden kann. |

### ReturnValue

Der Maßstab, der automatisch für die gerenderte Seite berechnet wurde, um die angegebene Größe zu passen.

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
