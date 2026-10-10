---
title: "Método Aspose::Words::Drawing::SignatureLine::get_SignerTitle"
linktitle: "get_SignerTitle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::SignatureLine::get_SignerTitle. Obtiene o establece el título sugerido del firmante (por ejemplo, Manager). El valor predeterminado para esta propiedad es cadena vacía en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.drawing/signatureline/get_signertitle/
---
## SignatureLine::get_SignerTitle method


Obtiene o establece el título del firmante sugerido (por ejemplo, Manager). El valor predeterminado para esta propiedad es **empty string**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_SignerTitle()
```


## Ejemplos



Muestra cómo crear una línea para una firma e insertarla en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// Inserte una forma que contendrá una línea de firma, cuya apariencia vamos a
// personalizar usando el objeto "SignatureLineOptions" que hemos creado arriba.
// Si insertamos una forma cuyas coordenadas se originan en la esquina inferior derecha de la página,
// necesitaremos proporcionar coordenadas x e y negativas para traer la forma a la vista.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Verifique las propiedades de nuestra línea de firma a través de su objeto Shape.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## Ver también

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
