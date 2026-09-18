---
title: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName Methode"
linktitle: "get_ExportGeneratorName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName Methode. Wenn true, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Der Standardwert ist true in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


Wenn **true**, wird der Name und die Version von Aspose.Words in die erzeugten Dateien eingebettet. Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Beispiele



Zeigt, wie das Hinzufügen von Name und Version von Aspose.Words in erzeugte Dateien deaktiviert werden kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Verwenden Sie https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/, um zu erfahren, wie das Ergebnis überprüft werden kann.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
