---
title: "Aspose::Words::Drawing::ShadowType enumeración"
linktitle: "ShadowType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShadowType enumeración. Especifica el tipo de sombra de una forma en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Especifica el tipo de sombra de una forma.

```cpp
enum class ShadowType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| ShadowMixed | -2 | Ninguno de los preajustes de sombra predefinidos. |
| Shadow1 | 1 | Primer tipo de sombra. |
| Shadow10 | 10 | Décimo tipo de sombra. |
| Shadow11 | 11 | Undécimo tipo de sombra. |
| Shadow12 | 12 | Duodécimo tipo de sombra. |
| Shadow13 | 13 | Decimotercer tipo de sombra. |
| Shadow14 | 14 | Decimocuarto tipo de sombra. |
| Shadow15 | 15 | Decimoquinto tipo de sombra. |
| Shadow16 | 16 | Decimosexto tipo de sombra. |
| Shadow17 | 17 | Decimoséptimo tipo de sombra. |
| Shadow18 | 18 | Decimoctavo tipo de sombra. |
| Shadow19 | 19 | Decimonoveno tipo de sombra. |
| Shadow2 | 2 | Segundo tipo de sombra. |
| Shadow20 | 20 | Vigésimo tipo de sombra. |
| Shadow21 | 21 | Vigésimo primer tipo de sombra. |
| Shadow22 | 22 | Tipo de sombra veintidós. |
| Shadow23 | 23 | Tipo de sombra veintitrés. |
| Shadow24 | 24 | Tipo de sombra veinticuatro. |
| Shadow25 | 25 | Tipo de sombra veinticinco. |
| Shadow26 | 26 | Tipo de sombra veintiséis. |
| Shadow27 | 27 | Tipo de sombra veintisiete. |
| Shadow28 | 28 | Tipo de sombra veintiocho. |
| Shadow29 | 29 | Tipo de sombra veintinueve. |
| Shadow3 | 3 | Tipo de sombra tercero. |
| Shadow30 | 30 | Tipo de sombra treinta. |
| Shadow31 | 31 | Tipo de sombra treinta y uno. |
| Shadow32 | 32 | Tipo de sombra treinta y dos. |
| Shadow33 | 33 | Tipo de sombra treinta y tres. |
| Shadow34 | 34 | Tipo de sombra treinta y cuatro. |
| Shadow35 | 35 | Tipo de sombra treinta y cinco. |
| Shadow36 | 36 | Tipo de sombra treinta y seis. |
| Shadow37 | 37 | Tipo de sombra treinta y siete. |
| Shadow38 | 38 | Tipo de sombra treinta y ocho. |
| Shadow39 | 39 | Tipo de sombra treinta y nueve. |
| Shadow4 | 4 | Cuarto tipo de sombra. |
| Shadow40 | 40 | Tipo de sombra cuarenta. |
| Shadow41 | 41 | Tipo de sombra cuarenta y uno. |
| Shadow42 | 42 | Tipo de sombra cuarenta y dos. |
| Shadow43 | 43 | Tipo de sombra cuarenta y tres. |
| Shadow5 | 5 | Quinto tipo de sombra. |
| Shadow6 | 6 | Sexto tipo de sombra. |
| Shadow7 | 7 | Séptimo tipo de sombra. |
| Shadow8 | 8 | Octavo tipo de sombra. |
| Shadow9 | 9 | Noveno tipo de sombra. |


## Ejemplos



Muestra cómo trabajar con un formato de sombra para la forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
