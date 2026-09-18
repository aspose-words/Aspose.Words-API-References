---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData Methode"
linktitle: "get_IgnoreOleData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData Methode. Gibt an, ob OLE-Daten in C++ ignoriert werden sollen."
type: docs
weight: 8000
url: /de/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


Gibt an, ob die OLE-Daten ignoriert werden sollen.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Hinweise


Das Ignorieren von OLE-Daten kann den Speicherverbrauch reduzieren und die Leistung steigern, ohne dass Daten verloren gehen, falls das Zielformat OLE-Objekte nicht unterstützt.

Der Standardwert ist **false**.

## Beispiele



Zeigt, wie OLE-Daten beim Laden ignoriert werden.
```cpp
// Das Ignorieren von OLE-Daten kann den Speicherverbrauch reduzieren und die Leistung steigern.
// ohne Datenverlust, falls das Zielformat OLE-Objekte nicht unterstützt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
