---
title: "Aspose::Words::ParagraphFormat::get_WidowControl método"
linktitle: "get_WidowControl"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_WidowControl método. Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


True si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Ejemplos



Muestra cómo habilitar el control de viudas/huérfanos para un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cuando escribimos el texto que no cabe en una página, una línea puede desbordarse a la página siguiente.
// La única línea que termina en la página siguiente se llama "huérfano",
// y la línea anterior donde se separó el huérfano se llama "viuda".
// Podemos corregir huérfanos y viudas reorganizando el texto mediante el tamaño de fuente, el espaciado o los márgenes de página.
// Si deseamos preservar las dimensiones de nuestro documento, podemos establecer esta bandera a "true"
// para mover las viudas a la misma página que sus respectivos huérfanos.
// Dejar esta bandera como "false" mantendrá los pares viuda/huérfano en el texto.
// Cada párrafo tiene esta configuración accesible en Microsoft Word a través de Inicio -> Párrafo -> Configuración de párrafo
// (botón en la esquina inferior derecha de la pestaña "Paragraph") -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Inserte texto que produzca un huérfano y una viuda.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
