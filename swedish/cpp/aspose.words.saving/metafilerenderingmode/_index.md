---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Anger hur Aspose.Words ska rendera WMF- och EMF-metafiler i C++."
type: docs
weight: 69000
url: /sv/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Anger hur Aspose.Words ska rendera WMF- och EMF-metafiler.

```cpp
enum class MetafileRenderingMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words försöker rendera en metafil som vektorgrafik. Om Aspose.Words inte kan korrekt rendera vissa av metafilens poster till vektorgrafik renderar Aspose.Words istället metafilen till en bitmap. |
| Vector | 1 | Aspose.Words renderar en metafil som vektorgrafik. |
| Bitmap | 2 | Aspose.Words anropar GDI+ för att rendera en metafil till en bitmap och sparar sedan bitmapen i utdata-dokumentet. |

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
