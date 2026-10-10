---
title: "Método Aspose::Words::Loading::LoadOptions::get_TempFolder"
linktitle: "get_TempFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_TempFolder. Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es null y no se utilizan archivos temporales en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Observaciones


La carpeta debe existir y ser escribible, de lo contrario se lanzará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando la lectura se completa.

## Ejemplos



Muestra cómo cargar un documento usando archivos temporales.
```cpp
// Tenga en cuenta que este enfoque puede reducir el uso de memoria pero degrada la velocidad.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Asegúrese de que el directorio exista y cargue
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Muestra cómo usar el disco duro en lugar de la memoria al cargar un documento.
```cpp
// Cuando cargamos un documento, varios elementos se almacenan temporalmente en la memoria mientras ocurre la operación de guardado.
// Podemos usar esta opción para utilizar una carpeta temporal en el sistema de archivos local en su lugar,
// lo que reducirá la sobrecarga de memoria de nuestra aplicación.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// La carpeta temporal especificada debe existir en el sistema de archivos local antes de la operación de carga.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// La carpeta persistirá sin contenidos residuales de la operación de carga.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
