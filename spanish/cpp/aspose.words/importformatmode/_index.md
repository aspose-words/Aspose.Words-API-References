---
title: "Aspose::Words::ImportFormatMode enumeración"
linktitle: "ImportFormatMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ImportFormatMode enumeración. Especifica cómo se combina el formato al importar contenido de otro documento en C++."
type: docs
weight: 93000
url: /es/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Especifica cómo se combina el formato al importar contenido de otro documento.

```cpp
enum class ImportFormatMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseDestinationStyles | 0 | Utiliza los estilos del documento de destino y copia los estilos nuevos. Esta es la opción predeterminada. |
| KeepSourceFormatting | 1 | Copie todos los estilos necesarios al documento de destino, genere nombres de estilo únicos si es necesario. |
| KeepDifferentStyles | 2 | Copiar solo los estilos que son diferentes de los del documento de origen. |

## Observaciones


Al copiar nodos de un documento a otro, esta opción especifica cómo se resuelve el formato cuando ambos documentos tienen un estilo con el mismo nombre, pero con formato diferente.

El formato se resuelve de la siguiente manera:

1. Los estilos incorporados se emparejan usando su identificador de estilo independiente de la configuración regional. Los estilos definidos por el usuario se emparejan usando el nombre del estilo sensible a mayúsculas y minúsculas.
1. Si no se encuentra un estilo coincidente en el documento de destino, el estilo (y todos los estilos referenciados por él) se copian al documento de destino y los nodos importados se actualizan para referenciar el nuevo estilo.
1. Si ya existe un estilo coincidente en el documento de destino, lo que ocurre depende del parámetro **importFormatMode** pasado a [ImportNode()](../) como se describe a continuación.



Al usar la opción [UseDestinationStyles](./), si ya existe un estilo coincidente en el documento de destino, el estilo no se copia y los nodos importados se actualizan para referenciar el estilo existente.

El inconveniente de usar [UseDestinationStyles](./) es que el texto importado puede verse diferente en el documento de destino en comparación con el documento de origen. Por ejemplo, el estilo \"Heading 1\" en el documento de origen usa la fuente Arial 16 pt y el estilo \"Heading 1\" en el documento de destino usa la fuente Times New Roman 14 pt. Al importar texto con el estilo \"Heading 1\" sin otro formato directo, aparecerá como Times New Roman 14 pt en el documento de destino.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

El inconveniente de usar [KeepSourceFormatting](./) es que, si realizas varias importaciones, podrías terminar con muchos estilos en el documento de destino y eso podría dificultar el uso de un formato de estilo coherente en Microsoft Word para este documento.

Usar la opción [KeepDifferentStyles](./) permite reutilizar los estilos de destino si el formato que proporcionan es idéntico al de los estilos en el documento de origen. Si el estilo en el documento de destino es diferente del origen, entonces se importa.

## Ejemplos



Muestra cómo insertar un documento en otro documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
