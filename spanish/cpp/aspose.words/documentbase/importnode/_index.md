---
title: "Método Aspose::Words::DocumentBase::ImportNode"
linktitle: "ImportNode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBase::ImportNode. Importa un nodo de otro documento al documento actual en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Importa un nodo de otro documento al documento actual.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo que se está importando. |
| isImportChildren | bool | **true** para importar todos los nodos hijos de forma recursiva; de lo contrario, **false**. |

### ReturnValue

El nodo clonado que pertenece al documento actual.
## Observaciones


Este método utiliza la opción [UseDestinationStyles](../../importformatmode/) para resolver el formato.

Importar un nodo crea una copia del nodo origen que pertenece al documento de importación. El nodo devuelto no tiene padre. El nodo origen no se altera ni se elimina del documento original.

Antes de que un nodo de otro documento pueda insertarse en este documento, debe importarse. Durante la importación, las propiedades específicas del documento, como referencias a estilos y listas, se traducen del original al documento de importación. Después de que el nodo se haya importado, puede insertarse en el lugar apropiado del documento usando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Si el nodo origen ya pertenece al documento de destino, simplemente se crea una clonación profunda del nodo origen.

## Ejemplos



Muestra cómo importar un nodo de un documento a otro.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Cada nodo tiene un documento padre, que es el documento que contiene al nodo.
// Insertar un nodo en un documento al que el nodo no pertenece lanzará una excepción.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// Utilice el método ImportNode para crear una copia de un nodo, que tendrá el documento
// que llamó al método ImportNode establecido como su nuevo documento propietario.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Ahora podemos insertar el nodo en el documento.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## Ver también

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Importa un nodo de otro documento al documento actual con una opción para controlar el formato.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo a importar. |
| isImportChildren | bool | **true** para importar todos los nodos hijos de forma recursiva; de lo contrario, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |

### ReturnValue

El nodo clonado e importado. El nodo pertenece al documento de destino, pero no tiene padre.
## Observaciones


Esta sobrecarga es útil para controlar cómo se importan los estilos y el formato de listas.

Importar un nodo crea una copia del nodo origen que pertenece al documento de importación. El nodo devuelto no tiene padre. El nodo origen no se altera ni se elimina del documento original.

Antes de que un nodo de otro documento pueda insertarse en este documento, debe importarse. Durante la importación, las propiedades específicas del documento, como referencias a estilos y listas, se traducen del original al documento de importación. Después de que el nodo se haya importado, puede insertarse en el lugar apropiado del documento usando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Si el nodo origen ya pertenece al documento de destino, simplemente se crea una clonación profunda del nodo origen.

## Ejemplos



Muestra cómo importar un nodo del documento origen al documento de destino con opciones específicas.
```cpp
// Cree dos documentos y agregue un estilo de carácter a cada documento.
// Configure los estilos para que tengan el mismo nombre, pero un formato de texto diferente.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Importe la Sección del documento de destino al documento origen, provocando una colisión de nombres de estilo.
// Si usamos los estilos de destino, entonces el texto origen importado con el mismo nombre de estilo
// como el texto de destino adoptará el estilo de destino.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// Si usamos ImportFormatMode.KeepDifferentStyles, el estilo origen se conserva,
// y el conflicto de nombres se resuelve añadiendo un sufijo.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## Ver también

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Importa un nodo de otro documento al documento actual con una opción para controlar el formato.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo a importar. |
| isImportChildren | bool | **true** para importar todos los nodos hijos de forma recursiva; de lo contrario, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Permite especificar varias opciones de formato adicionales. |

### ReturnValue

El nodo clonado e importado. El nodo pertenece al documento de destino, pero no tiene padre.
## Observaciones


Esta sobrecarga es útil para controlar cómo se importan los estilos y el formato de listas.

Importar un nodo crea una copia del nodo origen que pertenece al documento de importación. El nodo devuelto no tiene padre. El nodo origen no se altera ni se elimina del documento original.

Antes de que un nodo de otro documento pueda insertarse en este documento, debe importarse. Durante la importación, las propiedades específicas del documento, como referencias a estilos y listas, se traducen del original al documento de importación. Después de que el nodo se haya importado, puede insertarse en el lugar apropiado del documento usando [InsertBefore1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Si el nodo origen ya pertenece al documento de destino, simplemente se crea una clonación profunda del nodo origen.

## Ejemplos



Muestra cómo importar un nodo resolviendo los colores de tema origen de las formas.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Mueva al pie de página principal e inserte una forma que use los colores del tema.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importe el pie de página de origen al documento de destino con los colores del tema resueltos,
// para que la forma preserve su color real del documento de origen.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Ver también

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
