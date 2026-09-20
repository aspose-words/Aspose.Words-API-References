---
title: "Método Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate. Obtiene o establece el valor que indica si el texto bidireccional es totalmente compatible durante la actualización del campo o no en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Obtiene o establece el valor que indica si el texto bidireccional es totalmente compatible durante la actualización del campo o no.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Observaciones


Cuando esta propiedad se establece en **true**, se realizan pasos adicionales para producir un resultado de campo compatible con idiomas de derecha a izquierda (p. ej., árabe o hebreo) durante su actualización.

Cuando esta propiedad se establece en **false** y se utiliza un idioma de derecha a izquierda, no se garantiza la corrección del resultado del campo después de su actualización.

El valor predeterminado es **false**.

## Ejemplos



Muestra cómo usar [FieldOptions](../) para garantizar que la actualización de campos admita completamente el texto bidireccional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Asegúrese de que cualquier operación de campo que involucre texto de derecha a izquierda se realice según lo esperado.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Utilice un generador de documentos para insertar un campo que contiene texto de derecha a izquierda.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
