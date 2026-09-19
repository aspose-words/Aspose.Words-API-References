---
title: "Metodo Aspose::Words::Lists::ListLevel::GetEffectiveValue"
linktitle: "GetEffectiveValue"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Lists::ListLevel::GetEffectiveValue. Riporta la rappresentazione stringa dell'oggetto ListLevel per l'indice specificato dell'elemento dell'elenco. I parametri specificano il NumberStyle e una stringa di formato opzionale usata quando è specificato Custom in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Restituisce la rappresentazione testuale dell'oggetto [ListLevel](../) per l'indice specificato dell'elemento dell'elenco. I parametri specificano il [NumberStyle](../../../aspose.words/numberstyle/) e una stringa di formato opzionale utilizzata quando è specificato [Custom](../../../aspose.words/numberstyle/).

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice dell'elemento dell'elenco (deve essere nell'intervallo da 1 a 32767). |
| numberStyle | Aspose::Words::NumberStyle | Il [NumberStyle](../../../aspose.words/numberstyle/) dell'oggetto [ListLevel](../). |
| customNumberStyleFormat | const System::String\& | La stringa di formato opzionale usata quando è specificato [Custom](../../../aspose.words/numberstyle/) (ad es. "a, ç, ĝ, ..."). In altri casi, questo parametro deve essere **null** o vuoto. |

### ReturnValue

La rappresentazione stringa dell'oggetto [ListLevel](../), descritta dal parametro *numberStyle* e dal parametro *customNumberStyleFormat*, nell'elemento dell'elenco nella posizione determinata dal parametro *index*.

## Esempi



Mostra come ottenere il formato per un elenco con lo stile di numero personalizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Possiamo ottenere il valore per l'indice specificato dell'elemento dell'elenco.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## Vedi anche

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
