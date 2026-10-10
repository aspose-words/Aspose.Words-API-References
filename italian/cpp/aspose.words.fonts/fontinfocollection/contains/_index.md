---
title: "Metodo Aspose::Words::Fonts::FontInfoCollection::Contains"
linktitle: "Contains"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontInfoCollection::Contains. Determina se la collezione contiene un font con il nome specificato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Determina se la raccolta contiene un carattere con il nome specificato.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Nome del font non sensibile a maiuscole/minuscole da individuare. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

## Esempi



Mostra informazioni sui font presenti nel documento vuoto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene 3 font predefiniti. Ogni font nel documento
// avrà un oggetto FontInfo corrispondente che contiene i dettagli di quel font.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Vedi anche

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
