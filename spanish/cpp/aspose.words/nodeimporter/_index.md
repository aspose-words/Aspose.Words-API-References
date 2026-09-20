---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::NodeImporter class. Permite realizar de manera eficiente importaciones repetidas de nodos de un documento a otro. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 44000
url: /es/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Permite realizar de manera eficiente importaciones repetidas de nodos de un documento a otro. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeImporter : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importa un nodo de un documento a otro. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Inicializa una nueva instancia de la clase [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Inicializa una nueva instancia de la clase [NodeImporter](./). |
| static [Type](./type/)() |  |
## Observaciones


Aspose.Words proporciona funcionalidad para copiar y mover fácilmente fragmentos entre documentos de Microsoft Word. Esto se conoce como "importar nodos". Antes de poder insertar un fragmento de un documento en otro, necesita "importarlo". La importación crea un clon profundo del nodo original, listo para ser insertado en el documento de destino.

La forma más sencilla de importar un nodo es usar el método [ImportNode()](../) proporcionado por el objeto [DocumentBase](../documentbase/).

Sin embargo, cuando necesita importar nodos de un documento a otro varias veces, es mejor usar la clase [NodeImporter](./). La clase [NodeImporter](./) permite minimizar la cantidad de estilos y listas creadas en el documento de destino.

Copiar o mover fragmentos de un documento de Microsoft Word a otro presenta una serie de desafíos técnicos para Aspose.Words. En un documento de Word, los estilos y el formato de listas se almacenan de forma centralizada, separadamente del texto del documento. Los párrafos y corridas de texto simplemente hacen referencia a los estilos mediante identificadores internos únicos.

Los desafíos surgen del hecho de que los estilos y listas son diferentes en distintos documentos. Por ejemplo, para copiar un párrafo formateado con el estilo Heading 1 de un documento a otro, se deben tener en cuenta varios aspectos: decidir si se copia el estilo Heading 1 del documento origen al documento destino, clonar el párrafo, actualizar el párrafo clonado para que haga referencia al estilo Heading 1 correcto en el documento destino. Si el estilo debe copiarse, todos los estilos que referencia (basados en el estilo y el estilo del siguiente párrafo) deben analizarse y, posiblemente, copiarse también, y así sucesivamente. Problemas similares existen al copiar párrafos con viñetas o numerados porque Microsoft Word almacena las definiciones de listas por separado del texto.

La clase [NodeImporter](./) es como un contexto que mantiene las "tablas de traducción" durante la importación. Traduce correctamente entre estilos y listas en los documentos origen y destino.

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
