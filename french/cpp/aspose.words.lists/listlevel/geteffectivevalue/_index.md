---
title: "Méthode Aspose::Words::Lists::ListLevel::GetEffectiveValue"
linktitle: "GetEffectiveValue"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Lists::ListLevel::GetEffectiveValue. Signale la représentation sous forme de chaîne de l'objet ListLevel pour l'index spécifié de l'élément de liste. Les paramètres spécifient le NumberStyle et une chaîne de format optionnelle utilisée lorsque Custom est spécifié en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Renvoie la représentation sous forme de chaîne de l'objet [ListLevel](../) pour l'index spécifié de l'élément de liste. Les paramètres spécifient le [NumberStyle](../../../aspose.words/numberstyle/) et une chaîne de format optionnelle utilisée lorsque [Custom](../../../aspose.words/numberstyle/) est spécifié.

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | L'index de l'élément de liste (doit être compris entre 1 et 32767). |
| numberStyle | Aspose::Words::NumberStyle | Le [NumberStyle](../../../aspose.words/numberstyle/) de l'objet [ListLevel](../). |
| customNumberStyleFormat | const System::String\& | La chaîne de format optionnelle utilisée lorsque [Custom](../../../aspose.words/numberstyle/) est spécifié (par ex. "a, ç, ĝ, ..."). Dans les autres cas, ce paramètre doit être **null** ou vide. |

### ReturnValue

La représentation sous forme de chaîne de l'objet [ListLevel](../), décrite par le paramètre *numberStyle* et le paramètre *customNumberStyleFormat*, dans l'élément de liste à la position déterminée par le paramètre *index*.

## Exemples



Montre comment obtenir le format d'une liste avec le style de numéro personnalisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Nous pouvons obtenir la valeur pour l'index spécifié de l'élément de liste.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## Voir aussi

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
