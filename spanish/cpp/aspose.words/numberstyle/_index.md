---
title: "Aspose::Words::NumberStyle enumeración"
linktitle: "NumberStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::NumberStyle. Especifica el estilo de numeración para una lista, notas al pie y notas finales, números de página en C++."
type: docs
weight: 103000
url: /es/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Especifica el estilo de numeración para una lista, notas al pie y notas finales, números de página.

```cpp
enum class NumberStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Árabe | 0 | Numeración árabe (1, 2, 3, ...) |
| UppercaseRoman | 1 | Números romanos en mayúsculas (I, II, III, ...) |
| LowercaseRoman | 2 | Números romanos en minúsculas (i, ii, iii, ...) |
| UppercaseLetter | 3 | Letras mayúsculas (A, B, C, ...) |
| LowercaseLetter | 4 | Letras minúsculas (a, b, c, ...) |
| Ordinal | 5 | Ordinal (1.º, 2.º, 3.º, ...) |
| Number | 6 | Numerado (Uno, Dos, Tres, ...) |
| OrdinalText | 7 | Ordinal (texto) (Primero, Segundo, Tercero, ...) |
| Hex | 8 | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Manual de Chicago [Style](../style/): *, †, † |
| Kanji | 10 | Ideógrafo-digital. |
| KanjiDigit | 11 | Conteo japonés. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Árabe de ancho completo: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Árabe de medio ancho: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Legal japonés. |
| KanjiTraditional2 | 17 | Diez mil digital japonés. |
| NumberInCircle | 18 | Círculos encerrados. |
| DecimalFullWidth | 19 | Ancho completo decimal: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo ancho completo. |
| Iroha | 21 | Iroha ancho completo. |
| LeadingZero | 22 | Cero inicial (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Viñeta (verifique el código de carácter en el texto) |
| Ganada | 24 | Ganada coreano. |
| Chosung | 25 | Corea Chosung. |
| GB1 | 26 | Punto final encerrado. |
| GB2 | 27 | Paréntesis encerrado. |
| GB3 | 28 | Círculo chino encerrado. |
| GB4 | 29 | Ideograma círculo encerrado. |
| Zodiac1 | 30 | Ideograma tradicional. |
| Zodiac2 | 31 | Ideograma zodiacal. |
| Zodiac3 | 32 | Ideograma zodiacal tradicional. |
| TradChinNum1 | 33 | Conteo taiwanés. |
| TradChinNum2 | 34 | Ideógrafo legal tradicional. |
| TradChinNum3 | 35 | Conteo taiwanés de mil. |
| TradChinNum4 | 36 | Taiwanés digital. |
| SimpChinNum1 | 37 | Conteo chino. |
| SimpChinNum2 | 38 | Chino legal simplificado. |
| SimpChinNum3 | 39 | Conteo chino de mil. |
| SimpChinNum4 | 40 | Chino (no implementado) |
| HanjaRead | 41 | Coreano digital. |
| HanjaReadDigit | 42 | Conteo coreano. |
| Hangul | 43 | Corea legal. |
| Hanja | 44 | Corea digital2. |
| Hebrew1 | 45 | Hebreo-1. |
| Arabic1 | 46 | Árabe alfa. |
| Hebrew2 | 47 | Hebreo-2. |
| Arabic2 | 48 | Árabe abjad. |
| HindiLetter1 | 49 | Vocales hindi. |
| HindiLetter2 | 50 | Consonantes hindi. |
| HindiArabic | 51 | Números hindi. |
| HindiCardinalText | 52 | Descriptivo hindi (cardinales) |
| ThaiLetter | 53 | Letras tailandesas. |
| ThaiArabic | 54 | Números tailandeses. |
| ThaiCardinalText | 55 | Descriptivo tailandés (cardinales) |
| VietCardinalText | 56 | Descriptivo vietnamita (cardinales) |
| NumberInDash | 57 | Formato de número de página: - 1 -, - 2 -, - 3 -, - 4 -. |
| LowercaseRussian | 58 | Alfabeto ruso en minúsculas. |
| RusoMayúsculas | 59 | Alfabeto ruso en mayúsculas. |
| None | 255 | Sin viñeta ni número. |
| Personalizado | 65280 | Formato de número personalizado. Solo es compatible con el formato DOCX. |


## Ejemplos



Muestra cómo aplicar formato de lista personalizado a los párrafos al usar [DocumentBuilder](../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de la lista.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Este valor NumberFormat creará símbolos de viñetas en forma de estrella.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Cree párrafos y aplique ambos niveles de lista de nuestro formato de lista personalizado a ellos.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
