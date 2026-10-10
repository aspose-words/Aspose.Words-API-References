---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method"
linktitle: "get_LoadFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method. Especifica el formato del documento a cargar. El valor predeterminado es Auto en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Especifica el formato del documento a cargar. El valor predeterminado es [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Observaciones


Se recomienda que especifique el valor [Auto](../../../aspose.words/loadformat/) y permita que Aspose.Words detecte el formato del archivo automáticamente. Si conoce el formato del documento que está a punto de cargar, puede especificar el formato explícitamente y esto reducirá ligeramente el tiempo de carga al disminuir la sobrecarga asociada con la detección automática del formato. Si especifica un formato de carga explícito y resulta ser incorrecto, se invocará la detección automática y se realizará un segundo intento de cargar el archivo.

## Ejemplos



Muestra cómo especificar una URI base al abrir un documento html.
```cpp
// Supongamos que queremos cargar un documento .html que contiene una imagen vinculada mediante una URI relativa
// mientras la imagen está en una ubicación diferente. En ese caso, necesitaremos resolver la URI relativa en una absoluta.
// Podemos proporcionar una URI base usando un objeto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Aunque la imagen estaba rota en el .html de entrada, nuestra URI base personalizada nos ayudó a reparar el enlace.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Este documento de salida mostrará la imagen que faltaba.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Ver también

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
