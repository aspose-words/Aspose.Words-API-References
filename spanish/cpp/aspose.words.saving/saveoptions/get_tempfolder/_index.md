---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder método"
linktitle: "get_TempFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder método. Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. Por defecto, esta propiedad es null y no se utilizan archivos temporales en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Especifica la carpeta para archivos temporales usados al guardar en un archivo DOC o DOCX. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Observaciones


Cuando Aspose.Words guarda un documento, necesita crear estructuras internas temporales. Por defecto, estas estructuras internas se crean en memoria y el uso de memoria aumenta bruscamente por un corto período mientras se guarda el documento. Cuando la operación de guardado se completa, la memoria se libera y es recuperada por el recolector de basura.

Especificar una carpeta temporal usando [TempFolder](./) hará que Aspose.Words mantenga las estructuras internas en archivos temporales en lugar de en memoria. Reduce el uso de memoria durante el guardado, pero disminuirá el rendimiento del guardado.

La carpeta debe existir y ser escribible, de lo contrario se lanzará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando el guardado se completa.

## Ejemplos



Muestra cómo usar el disco duro en lugar de la memoria al guardar un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Cuando guardamos un documento, varios elementos se almacenan temporalmente en memoria mientras se lleva a cabo la operación de guardado.
// Podemos usar esta opción para utilizar una carpeta temporal en el sistema de archivos local en su lugar,
// lo que reducirá la sobrecarga de memoria de nuestra aplicación.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// La carpeta temporal especificada debe existir en el sistema de archivos local antes de la operación de guardado.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// La carpeta persistirá sin contenidos residuales de la operación de carga.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
