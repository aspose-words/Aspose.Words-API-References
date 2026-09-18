---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable Methode"
linktitle: "get_IsImageAvailable"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable Methode. Gibt true zurück, wenn das aktuelle Bild für den Export in C++ verfügbar ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Gibt **true** zurück, wenn das aktuelle Bild für den Export verfügbar ist.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Hinweise


Einige Bilder im Dokument können nicht verfügbar sein, zum Beispiel weil das Bild verlinkt ist und der Link nicht erreichbar ist oder nicht auf ein gültiges Bild verweist. In diesem Fall exportiert Aspose.Words ein Symbol mit einem roten Kreuz. Diese Eigenschaft gibt **true** zurück, wenn das Originalbild verfügbar ist; gibt **false** zurück, wenn das Originalbild nicht verfügbar ist und ein \"Kein Bild\"-Symbol zum Speichern angeboten wird.

Beim Speichern einer Gruppenkontur oder einer Form, die kein Bild benötigt, ist diese Eigenschaft immer **true**.

## Siehe auch

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
