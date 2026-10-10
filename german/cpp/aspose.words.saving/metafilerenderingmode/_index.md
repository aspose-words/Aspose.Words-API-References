---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Gibt an, wie Aspose.Words WMF- und EMF-Metadateien in C++ rendern soll."
type: docs
weight: 69000
url: /de/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Gibt an, wie Aspose.Words WMF- und EMF-Metadateien rendern soll.

```cpp
enum class MetafileRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words versucht, eine Metadatei als Vektorgrafik zu rendern. Wenn Aspose.Words einige der Metadatei‑Datensätze nicht korrekt in Vektorgrafiken rendern kann, rendert Aspose.Words diese Metadatei in ein Bitmap. |
| Vector | 1 | Aspose.Words rendert eine Metadatei als Vektorgrafiken. |
| Bitmap | 2 | Aspose.Words ruft GDI+ auf, um eine Metadatei in ein Bitmap zu rendern und speichert das Bitmap anschließend im Ausgabedokument. |

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
