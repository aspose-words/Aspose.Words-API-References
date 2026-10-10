---
title: "Constructor Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions. Inicializa una nueva instancia de esta clase con valores predeterminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Inicializa una nueva instancia de esta clase con valores predeterminados.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Ejemplos



Muestra cómo admitir comentarios condicionales al cargar un documento HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Si el valor es verdadero, entonces tenemos en cuenta el código VML al analizar el documento cargado.
loadOptions->set_SupportVml(supportVml);

// Este documento contiene una imagen JPEG dentro de las etiquetas \"<!--[if gte vml 1]>\" ,
// y una imagen PNG diferente dentro de las etiquetas \"<![if !vml]>\".
// Si establecemos la bandera \"SupportVml\" a \"true\", entonces Aspose.Words cargará el JPEG.
// Si establecemos esta bandera a \"false\", entonces Aspose.Words solo cargará el PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Ver también

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Un atajo para inicializar una nueva instancia de esta clase con las propiedades establecidas a los valores especificados.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | El formato del documento que se cargará. |
| password | const System::String\& | La contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. |
| baseUri | const System::String\& | La cadena que se usará para resolver URIs relativos a absolutos. Puede ser **null** o una cadena vacía. |

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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| password | const System::String\& | La contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. |

## Ejemplos



Muestra cómo cifrar un documento Html y luego abrirlo usando una contraseña.
```cpp
// Crea y firma un documento HTML cifrado a partir de un .docx cifrado.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Para cargar y leer este documento, necesitaremos pasar su descifrado
// contraseña usando un objeto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## Ver también

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
