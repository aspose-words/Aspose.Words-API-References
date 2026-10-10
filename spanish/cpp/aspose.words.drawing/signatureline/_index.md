---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::SignatureLine class. Proporciona acceso a las propiedades de la línea de firma. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Proporciona acceso a las propiedades de la línea de firma. Para obtener más información, visite el artículo de documentación [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLine : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Obtiene o establece un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Sign. El valor predeterminado para esta propiedad es **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Obtiene o establece un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Sign. El valor predeterminado para esta propiedad es **true**. |
| [get_Email](./get_email/)() | Obtiene o establece la dirección de correo electrónico sugerida del firmante. El valor predeterminado para esta propiedad es **empty string**. |
| [get_Id](./get_id/)() | Obtiene o establece el identificador para esta línea de firma. Este identificador puede asociarse con una firma digital, al firmar el documento usando [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). Este valor debe ser único y, por defecto, se genera aleatoriamente un nuevo Guid (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | Obtiene o establece las instrucciones para el firmante que se muestran al firmar la línea de firma. Esta propiedad se ignora si [DefaultInstructions](./get_defaultinstructions/) está establecida. El valor predeterminado para esta propiedad es **empty string**. |
| [get_IsSigned](./get_issigned/)() | Indica que la línea de firma está firmada con una firma digital. |
| [get_IsValid](./get_isvalid/)() | Indica que la línea de firma está firmada con una firma digital y que esta firma digital es válida. |
| [get_ProviderId](./get_providerid/)() | Obtiene o establece el identificador del proveedor de firma para esta línea de firma. El valor predeterminado es "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Obtiene o establece un valor que indica que la fecha de firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es **true**. |
| [get_Signer](./get_signer/)() | Obtiene o establece el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Obtiene o establece el título del firmante sugerido (por ejemplo, Manager). El valor predeterminado para esta propiedad es **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
