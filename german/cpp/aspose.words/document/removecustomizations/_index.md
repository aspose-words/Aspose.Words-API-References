---
title: "Aspose::Words::Document::RemoveCustomizations method"
linktitle: "RemoveCustomizations"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::RemoveCustomizations-Methode. Entfernt Toolbar- und Tastaturbefehlsanpassungen aus dem Dokument in C++."
type: docs
weight: 67750
url: /de/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Entfernt Toolbar‑ und Tastaturbefehlsanpassungen aus dem Dokument.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Beispiele



Zeigt, wie Toolbar- und Tastaturbefehlsanpassungen aus dem Dokument entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Entfernt alle benutzerdefinierten UI-Anpassungen des Dokuments, einschließlich benutzerdefinierter Kontextmenüeinträge.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
