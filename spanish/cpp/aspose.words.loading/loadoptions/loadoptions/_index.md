---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions constructor"
linktitle: "LoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions constructor. Inicializa una nueva instancia de esta clase con valores predeterminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Inicializa una nueva instancia de esta clase con valores predeterminados.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Ejemplos



Muestra cómo abrir un documento HTML con imágenes desde un flujo usando un URI base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Pase el URI de la carpeta base al cargarlo
    // para que cualquier imagen con URIs relativos en el documento HTML pueda ser encontrada.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verifique que la primera forma del documento contenga una imagen válida.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Un atajo para inicializar una nueva instancia de esta clase con las propiedades establecidas a los valores especificados.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| password | const System::String\& | La contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. |

## Ejemplos



Muestra cómo cargar un documento de Microsoft Word cifrado.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Al cargar dicho documento, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 -  Cargar el documento desde el sistema de archivos local mediante el nombre de archivo:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Cargar el documento desde un flujo:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
