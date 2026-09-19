---
title: "Aspose::Words::Document::RemoveCustomizations method"
linktitle: "RemoveCustomizations"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::RemoveCustomizations method. Rimuove le personalizzazioni della barra degli strumenti e dei comandi da tastiera dal documento in C++."
type: docs
weight: 67750
url: /it/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Rimuove le personalizzazioni della barra degli strumenti e dei comandi da tastiera dal documento.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Esempi



Mostra come rimuovere le personalizzazioni della barra degli strumenti e dei comandi da tastiera dal documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Rimuove tutte le personalizzazioni UI del documento, incluse le voci personalizzate del menu contestuale.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
