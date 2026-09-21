---
title: "Aspose::Words::Loading::ResourceLoadingAction enum"
linktitle: "ResourceLoadingAction"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::ResourceLoadingAction enum. Anger läget för resursladdning. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enum


Anger läget för resursladdning. För att lära dig mer, besök dokumentationsartikeln [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
enum class ResourceLoadingAction
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Standard | 0 | Aspose.Words kommer att ladda den här resursen som vanligt. |
| Hoppa över | 1 | Aspose.Words kommer att hoppa över laddning av den här resursen. Endast en länk utan data kommer att sparas för en bild, CSS-stilmallen kommer att ignoreras för HTML-format. |
| UserProvided | 2 | Aspose.Words kommer att använda bytearray som tillhandahålls av användaren i [SetData()](../) som resursdata. |

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
