---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault metodo"
linktitle: "get_TextInputDefault"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault metodo. Ottiene o imposta la stringa predefinita o un'espressione di calcolo di un campo modulo di testo in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Ottiene o imposta la stringa predefinita o un'espressione di calcolo di un campo modulo di testo.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Note


Il significato di questa proprietà dipende dal valore della proprietà [TextInputType](../get_textinputtype/).

Quando [TextInputType](../get_textinputtype/) è [Regular](../../textformfieldtype/) o [Number](../../textformfieldtype/), questa stringa specifica la stringa predefinita per il campo modulo di testo. Questa stringa è il contenuto che Microsoft Word visualizzerà nel documento quando il campo modulo è vuoto.

Quando [TextInputType](../get_textinputtype/) è [Calculated](../../textformfieldtype/), questa stringa contiene l'espressione da calcolare. L'espressione deve essere una formula valida secondo i requisiti dei campi formula di Microsoft Word. Quando imposti una nuova espressione utilizzando questa proprietà, Aspose.Words calcola automaticamente il risultato della formula e lo inserisce nel campo modulo.

Microsoft Word consente stringhe di al massimo 255 caratteri.
## Vedi anche

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
