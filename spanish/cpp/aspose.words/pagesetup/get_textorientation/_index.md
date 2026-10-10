---
title: "Método Aspose::Words::PageSetup::get_TextOrientation"
linktitle: "get_TextOrientation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_TextOrientation. Permite especificar TextOrientation para toda la página. El valor predeterminado es Horizontal en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Permite especificar [TextOrientation](./) para toda la página. El valor predeterminado es [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Ejemplos



Muestra cómo establecer la orientación del texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Establezca la propiedad "TextOrientation" a "TextOrientation.Upward" para rotar todo el texto 90 grados
// hacia la derecha para que todo el texto de izquierda a derecha ahora vaya de arriba a abajo.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## Ver también

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
