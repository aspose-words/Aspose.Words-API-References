---
title: "Aspose::Words::Lists::ListTemplate enum"
linktitle: "ListTemplate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListTemplate enum. Especifica uno de los formatos de lista predefinidos disponibles en Microsoft Word en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


Especifica uno de los formatos de lista predefinidos disponibles en Microsoft Word.

```cpp
enum class ListTemplate
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| BulletDefault | 0 | Lista con viñetas predeterminada con 9 niveles. La viñeta del primer nivel es un disco, la viñeta del segundo nivel es un círculo, la viñeta del tercer nivel es un cuadrado. Luego el formato se repite para los niveles restantes. Cada nivel está sangrado a la derecha 0.25\" respecto al nivel anterior. Corresponde a la primera plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| BulletDisk | n/a | Igual que [BulletDefault](./). Corresponde a la primera plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| BulletCircle | n/a | La viñeta del primer nivel es un círculo. Los niveles restantes son iguales que en [BulletDefault](./). Corresponde a la segunda plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| BulletSquare | n/a | La viñeta del primer nivel es un cuadrado. Los niveles restantes son iguales que en [BulletDefault](./). Corresponde a la tercera plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| BulletDiamonds | n/a | La viñeta del primer nivel es un carácter Wingding de 4 diamantes. Los niveles restantes son iguales que en [BulletDefault](./). Corresponde a la quinta plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| BulletArrowHead | n/a | La viñeta del primer nivel es un carácter Wingding de cabeza de flecha. Los niveles restantes son iguales que en [BulletDefault](./). Corresponde a la sexta plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| BulletTick | n/a | La viñeta del primer nivel es un carácter Wingding de marca de verificación. Los niveles restantes son iguales que en [BulletDefault](./). Corresponde a la séptima plantilla de lista con viñetas en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberDefault | n/a | Lista numerada predeterminada con 9 niveles. Numeración arábiga (1., 2., 3., ...) para el primer nivel, numeración con letras minúsculas (a., b., c., ...) para el segundo nivel, numeración romana en minúsculas (i., ii., iii., ...) para el tercer nivel. Luego el formato se repite para los niveles restantes. Cada nivel está sangrado a la derecha 0.25\" respecto al nivel anterior. Corresponde a la primera plantilla de lista numerada en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberArabicDot | n/a | Igual que [NumberDefault](./). Corresponde a la primera plantilla de lista numerada en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberArabicParenthesis | n/a | El número del primer nivel es "1)". Los niveles restantes son iguales que en [NumberDefault](./). Corresponde a la segunda plantilla de lista numerada en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberUppercaseRomanDot | n/a | El número del primer nivel es "I.". Los niveles restantes son iguales que en [NumberDefault](./). Corresponde a la tercera plantilla de lista numerada en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberUppercaseLetterDot | n/a | El número del primer nivel es "A.". Los niveles restantes son iguales que en [NumberDefault](./). Corresponde a la cuarta plantilla de lista numerada en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberLowercaseLetterParenthesis | n/a | El número del primer nivel es "a)". Los niveles restantes son iguales que en [NumberDefault](./). Corresponde a la quinta plantilla de lista numerada en el cuadro de diálogo Viñetas y Numeración de Microsoft Word. |
| NumberLowercaseLetterDot | n/a | El número del primer nivel es "a.". Los niveles restantes son iguales que en [NumberDefault](./). Corresponde a la sexta plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| NumberLowercaseRomanDot | n/a | El número del primer nivel es "i.". Los niveles restantes son iguales que en [NumberDefault](./). Corresponde a la séptima plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineNumbers | n/a | Una lista de esquema con niveles numerados "1), a), i), (1), (a), (i), 1., a., i.". Corresponde a la primera plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineLegal | n/a | Una lista de esquema con niveles numerados "1., 1.1., 1.1.1, ...". Corresponde a la segunda plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineBullets | n/a | Una lista de esquema con viñetas variadas para diferentes niveles. Corresponde a la tercera plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineHeadingsArticleSection | n/a | Una lista de esquema con niveles vinculados a los estilos de título. Corresponde a la cuarta plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineHeadingsLegal | n/a | Una lista de esquema con niveles vinculados a los estilos de título. Corresponde a la quinta plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineHeadingsNumbers | n/a | Una lista de esquema con niveles vinculados a los estilos de título. Corresponde a la sexta plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |
| OutlineHeadingsChapter | n/a | Una lista de esquema con niveles vinculados a los estilos de título. Corresponde a la séptima plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word. |

## Observaciones


Un valor de plantilla de lista se usa como parámetro en el método [Add()](../listcollection/add/).

Las plantillas de lista de Aspose.Words corresponden a las 21 plantillas de lista disponibles en el cuadro de diálogo Viñetas y numeración de Microsoft Word 2003.

## Ejemplos



Muestra cómo trabajar con niveles de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación se presentan dos tipos de listas que podemos crear usando un document builder.
// 1 -  Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para iniciar una sublista autocontenida en el elemento de lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
// Los niveles de lista más profundos usan letras y números romanos en minúscula.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista usarán símbolos diferentes, como "■" y "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Podemos desactivar el formato de lista para que no formatee los párrafos subsecuentes como listas desactivando la bandera "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Muestra cómo reiniciar la numeración en una lista copiando una lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Crea una lista a partir de una plantilla de Microsoft Word y personaliza su primer nivel de lista.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Aplica nuestra lista a algunos párrafos.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Podemos agregar una copia de una lista existente a la colección de listas del documento
// para crear una lista similar sin hacer cambios en la original.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Aplica la segunda lista a nuevos párrafos.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Ver también

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
