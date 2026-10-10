---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_PreProcessCulture"
linktitle: "get_PreProcessCulture"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_PreProcessCulture. Ottiene o imposta la cultura per pre-elaborare i valori dei campi in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Ottiene o imposta la cultura per pre-elaborare i valori dei campi.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Note


Attualmente questa proprietà influisce solo sul valore del campo [FieldDocProperty](../../fielddocproperty/).

Il valore predefinito è **null**. Quando questa proprietà è impostata su **null**, il valore del campo [FieldDocProperty](../../fielddocproperty/) viene pre-elaborato con la cultura controllata dalla proprietà [FieldUpdateCultureSource](../get_fieldupdateculturesource/).

## Esempi



Mostra come impostare la cultura di pre-elaborazione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta la cultura in base alla quale alcuni campi formatteranno i loro valori visualizzati.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// Il campo DOCPROPERTY visualizzerà il suo risultato formattato secondo la cultura di pre-elaborazione
// che abbiamo impostato su tedesco. Il campo visualizzerà la data/ora usando il formato "dd.mm.yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// Dopo aver cambiato alla cultura invariata, il campo DOCPROPERTY utilizzerà il formato "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## Vedi anche

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
