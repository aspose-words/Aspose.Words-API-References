---
title: "Método Aspose::Words::Document::AppendDocument"
linktitle: "AppendDocument"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::AppendDocument. Añade el documento especificado al final de este documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Añade el documento especificado al final de este documento.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | El documento a añadir. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |

## Ejemplos



Muestra cómo añadir un documento al final de otro documento.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Añade el documento de origen al documento de destino mientras preserva su formato,
// luego guarda el documento de origen en el sistema de archivos local.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Muestra cómo añadir todos los documentos de una carpeta al final de un documento plantilla.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Añade todos los documentos sin cifrar con la extensión .doc
// desde nuestro directorio del sistema de archivos local al documento base.
System::SharedPtr<System::Collections::Generic::List<System::String>> docFiles = System::IO::Directory::GetFiles(get_MyDir(), u"*.doc")->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String item)>>([](System::String item) -> bool
{
    return item.EndsWith(u".doc");
})))->LINQ_ToList();
for (auto&& fileName : docFiles)
{
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(fileName);
    if (info->get_IsEncrypted())
    {
        continue;
    }

    auto srcDoc = System::MakeObject<Aspose::Words::Document>(fileName);
    dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles);
}

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendAllDocumentsInFolder.doc");
```

## Ver también

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Añade el documento especificado al final de este documento.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | El documento a añadir. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Permite especificar opciones que afectan el formato de un documento resultante. |

## Ejemplos



Muestra cómo gestionar conflictos de estilo de lista al añadir un documento.
```cpp
// Carga un documento con texto en un estilo personalizado y clónalo.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Ahora tenemos dos documentos, cada uno con un estilo idéntico llamado "CustomStyle".
// Cambia el color del texto de uno de los estilos para distinguirlo del otro.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// Si hay un conflicto de estilos de lista, aplica el formato de lista del documento de origen.
// Establece la propiedad "KeepSourceNumbering" a "false" para no importar ningún número de lista al documento de destino.
// Establece la propiedad "KeepSourceNumbering" a "true" para importar todo lo que entra en conflicto
// numeración de estilo de lista con la misma apariencia que tenía en el documento de origen.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Unir dos documentos que tienen estilos diferentes que comparten el mismo nombre provoca un conflicto de estilo.
// Podemos especificar un modo de formato de importación al añadir documentos para resolver este conflicto.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Muestra cómo gestionar conflictos de estilo de lista al insertar un documento.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

dstDoc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
System::SharedPtr<Aspose::Words::Lists::List> list = dstDoc->get_Lists()->idx_get(0);

builder->get_ListFormat()->set_List(list);

for (int32_t i = 1; i <= 15; i++)
{
    builder->Write(System::String::Format(u"List Item {0}\n", i));
}

auto attachDoc = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(dstDoc)->Clone(true));

// Si hay un conflicto de estilos de lista, aplica el formato de lista del documento de origen.
// Establece la propiedad "KeepSourceNumbering" a "false" para no importar ningún número de lista al documento de destino.
// Establece la propiedad "KeepSourceNumbering" a "true" para importar todo lo que entra en conflicto
// numeración de estilo de lista con la misma apariencia que tenía en el documento de origen.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Muestra cómo gestionar conflictos de estilo de lista al añadir un clon de un documento a sí mismo.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Si hay un conflicto de estilos de lista, aplica el formato de lista del documento de origen.
// Establece la propiedad "KeepSourceNumbering" a "false" para no importar ningún número de lista al documento de destino.
// Establece la propiedad "KeepSourceNumbering" a "true" para importar todo lo que entra en conflicto
// numeración de estilo de lista con la misma apariencia que tenía en el documento de origen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## Ver también

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
