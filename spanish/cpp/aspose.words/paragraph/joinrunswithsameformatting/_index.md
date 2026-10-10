---
title: "Método Aspose::Words::Paragraph::JoinRunsWithSameFormatting"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Paragraph::JoinRunsWithSameFormatting. Une segmentos con el mismo formato en el párrafo en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Une ejecuciones con el mismo formato en el párrafo.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Número de uniones realizadas. Cuando se unen **N** runs adyacentes, cuentan como **N - 1** uniones.

## Ejemplos



Muestra cómo simplificar párrafos combinando segmentos superfluos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta cuatro segmentos de texto en el párrafo.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Si abrimos este documento en Microsoft Word, el párrafo se verá como un cuerpo de texto continuo.
// Sin embargo, constará de cuatro segmentos separados con el mismo formato. Párrafos fragmentados como este
// pueden ocurrir cuando editamos manualmente partes de un párrafo muchas veces en Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Cambia el estilo del último segmento para diferenciarlo de los tres primeros.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// Podemos ejecutar el método "JoinRunsWithSameFormatting" para optimizar el contenido del documento
// uniendo segmentos similares en uno, reduciendo su número total.
// Este método también devuelve el número de segmentos que este método fusionó.
// Estas dos fusiones se realizaron para combinar los Segmentos #1, #2 y #3,
// omitiendo Run #4 porque tiene un estilo incompatible.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// El número de ejecuciones restantes será igual al recuento original
// menos el número de combinaciones de ejecuciones que el método "JoinRunsWithSameFormatting" realizó.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## Ver también

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Une ejecuciones con el mismo formato en el párrafo.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| opciones | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Opciones adicionales |

### ReturnValue

Número de uniones realizadas. Cuando se unen **N** runs adyacentes, cuentan como **N - 1** uniones.

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

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
