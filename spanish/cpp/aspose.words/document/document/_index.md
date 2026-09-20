---
title: "Aspose::Words::Document::Document constructor"
linktitle: "Documento"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::Document constructor. Crea un documento Word en blanco en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Crea un documento Word en blanco.

```cpp
Aspose::Words::Document::Document()
```

## Observaciones


Se obtiene un documento en blanco de los recursos, y por defecto, el documento resultante se parece más a uno creado por [Word2007](../../../aspose.words.settings/mswordversion/). Este documento en blanco contiene una tabla de fuentes predeterminada, estilos predeterminados mínimos y estilos latentes.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

El tamaño de papel del documento es Letter por defecto. Si desea cambiar la configuración de página, use [PageSetup](../../section/get_pagesetup/).

Después de la creación, puedes usar [DocumentBuilder](../../documentbuilder/) para agregar contenido del documento fácilmente.

## Ejemplos



Muestra cómo crear un documento simple.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Los nuevos objetos Document por defecto vienen con el conjunto mínimo de nodos
// requeridos para comenzar a agregar contenido como texto y formas: una Section, un Body y un Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Muestra cómo crear y cargar documentos.
```cpp
// Hay dos formas de crear un objeto Document usando Aspose.Words.
// 1 -  Crear un documento en blanco:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Los nuevos objetos Document por defecto vienen con el conjunto mínimo de nodos
// requeridos para comenzar a agregar contenido como texto y formas: una Section, un Body y un Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Cargar un documento que existe en el sistema de archivos local:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Los documentos cargados tendrán contenidos a los que podemos acceder y editar.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Algunas operaciones que deben ocurrir durante la carga, como usar una contraseña para descifrar un documento,
// pueden realizarse pasando un objeto LoadOptions al cargar el documento.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Muestra cómo formatear una corrida de texto usando su propiedad de fuente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Abre un documento existente desde un flujo. Detecta automáticamente el formato del archivo.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Flujo desde el cual cargar el documento. |
## Observaciones


El documento debe estar almacenado al comienzo del flujo. El flujo debe soportar posicionamiento aleatorio.

## Ejemplos



Muestra cómo cargar un documento usando un flujo.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Abre un documento existente desde un flujo. Permite especificar opciones adicionales como una contraseña de cifrado.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo desde el cual cargar el documento. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Opciones adicionales para usar al cargar un documento. Puede ser **null**. |
## Observaciones


El documento debe estar almacenado al comienzo del flujo. El flujo debe soportar posicionamiento aleatorio.

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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Abre un documento existente desde un archivo. Detecta automáticamente el formato del archivo.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Nombre de archivo del documento a abrir. |

## Ejemplos



Muestra cómo abrir un documento y convertirlo a .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Abre un documento existente desde un archivo. Permite especificar opciones adicionales como una contraseña de cifrado.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Nombre de archivo del documento a abrir. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Opciones adicionales para usar al cargar un documento. Puede ser **null**. |

## Ejemplos



Muestra cómo crear y cargar documentos.
```cpp
// Hay dos formas de crear un objeto Document usando Aspose.Words.
// 1 -  Crear un documento en blanco:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Los nuevos objetos Document por defecto vienen con el conjunto mínimo de nodos
// requeridos para comenzar a agregar contenido como texto y formas: una Section, un Body y un Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Cargar un documento que existe en el sistema de archivos local:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Los documentos cargados tendrán contenidos a los que podemos acceder y editar.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Algunas operaciones que deben ocurrir durante la carga, como usar una contraseña para descifrar un documento,
// pueden realizarse pasando un objeto LoadOptions al cargar el documento.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
