---
title: "Aspose::Words::Font::get_StyleIdentifier método"
linktitle: "get_StyleIdentifier"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_StyleIdentifier. Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words/font/get_styleidentifier/
---
## Font::get_StyleIdentifier method


Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Font::get_StyleIdentifier()
```


## Ejemplos



Muestra cómo cambiar el estilo del texto existente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de referenciar estilos.
// 1 -  Usando el nombre de estilo:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Usando un identificador de estilo incorporado:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Convertir todos los usos de un estilo a otro,
// usando los métodos anteriores para referenciar estilos antiguos y nuevos.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## Ver también

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
