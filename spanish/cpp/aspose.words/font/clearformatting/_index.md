---
title: "Método Aspose::Words::Font::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::ClearFormatting. Restablece el formato de fuente predeterminado en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Restablece el formato de fuente predeterminado.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Observaciones


Elimina todo el formato de fuente especificado explícitamente en el objeto del que se obtuvo [Font](../) para que el formato de fuente se herede del padre apropiado.

## Ejemplos



Muestra cómo insertar un campo de hipervínculo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto clicable que nos llevará a la ubicación especificada en la URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL mediante una nueva ventana del navegador web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
