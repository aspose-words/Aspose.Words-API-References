---
title: "Constructor Aspose::Words::NodeImporter::NodeImporter"
linktitle: "NodeImporter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::NodeImporter::NodeImporter. Inicializa una nueva instancia de la clase NodeImporter en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Inicializa una nueva instancia de la clase [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento de origen. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento de destino que será el propietario de los nodos importados. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |

## Ver también

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Inicializa una nueva instancia de la clase [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento de origen. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento de destino que será el propietario de los nodos importados. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Especifica varias opciones para formatear el nodo importado. |

## Ejemplos



Muestra cómo resolver un conflicto al importar documentos que tienen listas con el mismo identificador de definición de lista.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Establece la propiedad "KeepSourceNumbering" a "true" para aplicar un ID de definición de lista diferente
// a estilos idénticos como Aspose.Words los importa en los documentos destino.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Muestra cómo resolver conflictos de numeración de listas en los documentos origen y destino.
```cpp
// Abre un documento con un esquema de numeración de lista personalizado, y luego clónalo.
// Dado que ambos tienen el mismo formato de numeración, los formatos entrarán en conflicto si importamos un documento en el otro.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Cuando importamos el clon del documento al original y luego lo añadimos,
// entonces las dos listas con el mismo formato de lista se unirán.
// Si establecemos la bandera "KeepSourceNumbering" a "false", entonces la lista del clon del documento
// que añadimos al original continuará con la numeración de la lista a la que la añadimos.
// Esto fusionará efectivamente las dos listas en una.
// Si establecemos la bandera "KeepSourceNumbering" a "true", entonces el clon del documento
// la lista conservará su numeración original, haciendo que las dos listas aparezcan como listas separadas.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## Ver también

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
