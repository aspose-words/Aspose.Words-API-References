---
title: "Clase Aspose::Words::JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::JoinRunsOptions. Proporciona banderas de configuración para la operación de unión de ejecuciones en C++."
type: docs
weight: 38500
url: /es/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Proporciona indicadores de configuración para la operación de unión de ejecuciones.

```cpp
class JoinRunsOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | Verdadero indica que los atributos insignificantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | Verdadero indica que los atributos redundantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | Verdadero indica que los atributos de espaciado de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | Verdadero indica que los atributos insignificantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | Verdadero indica que los atributos redundantes de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | Verdadero indica que los atributos de espaciado de todas las ejecuciones serán ignorados al unir ejecuciones con el mismo formato. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo unir ejecuciones con el mismo formato mientras se ignoran los atributos redundantes e insignificantes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea ejecuciones con formato visible idéntico pero con algunas diferencias internas.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Verifica las ejecuciones antes de la unión.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Configura opciones para ignorar atributos redundantes e insignificantes durante la unión.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignora propiedades redundantes de la ejecución que no afectan la apariencia.
options->set_IgnoreInsignificant(true);
// Ignora diferencias insignificantes como ejecuciones que solo contienen espacios en blanco.

// Unir fragmentos que tengan el mismo formato visible usando las opciones extendidas.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Verifique que los fragmentos se hayan unido correctamente.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
