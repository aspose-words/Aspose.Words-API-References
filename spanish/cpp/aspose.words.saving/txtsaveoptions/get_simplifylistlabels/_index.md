---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels método"
linktitle: "get_SimplifyListLabels"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels método. Especifica si el programa debe simplificar las etiquetas de lista en caso de que el formato complejo de las etiquetas no se represente adecuadamente en texto plano. Si se establece en true, las etiquetas de listas numeradas se escriben en formato numérico simple y las etiquetas de listas con viñetas como caracteres ASCII simples. El valor predeterminado es false en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Especifica si el programa debe simplificar las etiquetas de lista en caso de que el formato complejo de etiquetas no se represente adecuadamente en texto plano. Si se establece en **true**, las etiquetas de listas numeradas se escriben en formato numérico simple y las etiquetas de listas con viñetas como caracteres ASCII simples. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Ejemplos



Muestra cómo cambiar la apariencia de las listas al guardar un documento como texto plano.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree una lista con viñetas con cinco niveles de sangría.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Establezca la propiedad "SimplifyListLabels" en "true" para convertir algunas listas
// símbolos en caracteres ASCII más simples, como '*', 'o', '+', '>', etc.
// Establezca la propiedad "SimplifyListLabels" en "false" para preservar la mayor cantidad posible de símbolos originales de la lista.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## Ver también

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
