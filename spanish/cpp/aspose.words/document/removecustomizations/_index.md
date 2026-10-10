---
title: "Aspose::Words::Document::RemoveCustomizations method"
linktitle: "RemoveCustomizations"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::RemoveCustomizations. Elimina las personalizaciones de la barra de herramientas y los comandos del teclado del documento en C++."
type: docs
weight: 67750
url: /es/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Elimina las personalizaciones de la barra de herramientas y los comandos del teclado del documento.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Ejemplos



Muestra cómo eliminar las personalizaciones de la barra de herramientas y los comandos del teclado del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Elimina todas las personalizaciones de la interfaz de usuario del documento, incluidas las entradas personalizadas del menú contextual.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
