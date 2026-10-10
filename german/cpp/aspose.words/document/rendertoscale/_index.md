---
title: "Aspose::Words::Document::RenderToScale method"
linktitle: "RenderToScale"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::RenderToScale-Methode. Rendert eine Dokumentenseite in ein Graphics-Objekt mit einem angegebenen Maßstab in C++."
type: docs
weight: 70000
url: /de/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Rendert eine Dokumentseite in ein **Graphics**‑Objekt mit einem angegebenen Maßstab.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | int32_t | Der 0-basierte Seitenindex. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Das Objekt, in das gerendert werden soll. |
| x | float | Die X‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| y | float | Die Y‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| scale | float | Der Maßstab für das Rendern der Seite (1,0 entspricht 100 %). |

### ReturnValue

Die Breite und Höhe (in Welteinheiten) der gerenderten Seite.

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
