---
title: "Aspose::Words::ParagraphFormat::get_SuppressLineNumbers método"
linktitle: "get_SuppressLineNumbers"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_SuppressLineNumbers método. Especifica si las líneas del párrafo actual'' deben estar exentas de la numeración de líneas que se aplica en la sección principal en C++."
type: docs
weight: 39000
url: /es/cpp/aspose.words/paragraphformat/get_suppresslinenumbers/
---
## ParagraphFormat::get_SuppressLineNumbers method


Especifica si las líneas del párrafo actual deben estar exentas de la numeración de líneas que se aplica en la sección principal.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressLineNumbers()
```


## Ejemplos



Muestra cómo habilitar la numeración de líneas para una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Podemos usar el objeto PageSetup de la sección para mostrar los números a la izquierda de las líneas de texto de la sección.
// Este es el mismo comportamiento que un objeto List,
// pero cubre toda la sección y no modifica el texto de ninguna manera.
// Nuestra sección reiniciará la numeración en cada página nueva desde 1 y mostrará el número,
// si es múltiplo de 3, a 50pt a la izquierda de la línea.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// El contador de líneas omitirá cualquier párrafo con la bandera "SuppressLineNumbers" establecida en "true".
// Este párrafo está en la línea 15, que es múltiplo de 3, y por lo tanto normalmente mostraría un número de línea.
// El contador de líneas de la sección también ignorará esta línea, tratará la siguiente línea como la 15ª,
// y continuará la cuenta a partir de ese punto.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
