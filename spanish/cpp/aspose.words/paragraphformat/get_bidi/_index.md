---
title: "Aspose::Words::ParagraphFormat::get_Bidi método"
linktitle: "get_Bidi"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_Bidi método. Obtiene o establece si este es un párrafo de derecha a izquierda en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Obtiene o establece si este es un párrafo de derecha a izquierda.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Observaciones


Cuando **true**, los fragmentos y otros objetos en línea en este párrafo se disponen de derecha a izquierda.

## Ejemplos



Muestra cómo crear listas compatibles con idiomas de derecha a izquierda usando campos BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// El campo BIDIOUTLINE numera párrafos como los campos AUTONUM/LISTNUM,
// pero solo es visible cuando se habilita un idioma de edición de derecha a izquierda, como hebreo o árabe.
// El siguiente campo mostrará ".1", el equivalente RTL del número de lista "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Agregue dos campos BIDIOUTLINE más, que mostrarán ".2" y ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Establezca la alineación horizontal del texto para cada párrafo del documento en RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Si habilitamos un idioma de edición de derecha a izquierda en Microsoft Word, nuestros campos mostrarán números.
// De lo contrario, mostrarán "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Muestra cómo detectar la dirección del texto en un documento de texto plano.
```cpp
// Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar cómo cargamos un documento de texto plano.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Establezca la propiedad "DocumentDirection" a "DocumentDirection.Auto" para detectar automáticamente
// la dirección de cada párrafo de texto que Aspose.Words carga desde texto plano.
// La propiedad "Bidi" de cada párrafo almacenará su dirección.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Detectar texto hebreo como de derecha a izquierda.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Detectar texto inglés como de derecha a izquierda.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
